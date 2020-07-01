# test_practice_with_nodejs_and_mocha_chai
Test básico de prueba con Node js - Mocha y Chai

Primer test básico en JavaScript , usando Node Js, Mocha y Chai.

Para correr el test se requeire Node Js instalado y el manager de paquetes npm, ademas de los frameworks Mocha.js y Chai.js.

El test se corre con el siguiente comando:
  npm test
 
 Explicación:
 
 En el archivo calculator-tests.js se puede ver en la parte superior las importaciones necesarias para las pruebas:
 
  var chai = require('chai'); /* Se importa Chai */
  var assert = chai.assert; /* Se importa la funcionalidad assert */
  var should = chai.should(); /* Se importa la funcionalidad should */
  var expect = chai.expect; /* Se importa la funcionalidad expect */
  var calculator = require('../calculator'); /* Se importa el archivo calculator que está en el mismo proyecto */
  
  /* Los tres test hacen lo mismo, solo que usando cada una de las tres funcionalidades immportadas anteriormente. 
     El test se trata de verificar el resultado de una suma sencilla */
  
  describe('Testing assert function: ', function() {
  describe('Check addTest Function', function(){
    it('Check the returned value using : assert.equal(value, value): ', function() {
       result = calculator.addTest(1,1);
       assert.equal(result, 2);
    });
  });
})

describe('Testing should function: ', function() {
    describe('Check addTest Function', function(){
      it('Check the returned value using : result.should.be.equal(value): ', function() {
         result = calculator.addTest(1,1);
         result.should.be.equal(2);
      })
    })
  })

  describe('Testing expect function: ', function() {
    describe('Check addTest Function', function(){
      it('Check the returned value using : expect(result).to.be.a(value);: ', function() {
         result = calculator.addTest(1,1);
          expect(result).to.equal(2);
      })
    })
  })

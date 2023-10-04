// Classe ContaBancaria
class ContaBancaria {
    constructor(agencia, numero, tipo, saldo) {
        this.agencia = agencia;
        this.numero = numero;
        this.tipo = tipo;
        this.saldo = saldo;
    }

    getSaldo() {
        return this.saldo;
    }

    setSaldo(valor) {
        this.saldo = valor;
    }

    sacar(valor) {
        if (valor <= this.saldo) {
            this.saldo -= valor;
            return true;
        }
        return false;
    }

    depositar(valor) {
        if (valor > 0) {
            this.saldo += valor;
            return true;
        }
        return false;
    }
}

// Classe ContaCorrente (Herda de ContaBancaria)
class ContaCorrente extends ContaBancaria {
    constructor(agencia, numero, saldo, cartaoCredito) {
        super(agencia, numero, "Conta Corrente", saldo);
        this.cartaoCredito = cartaoCredito;
    }

    getCartaoCredito() {
        return this.cartaoCredito;
    }

    setCartaoCredito(valor) {
        this.cartaoCredito = valor;
    }
}

// Classe ContaPoupanca (Herda de ContaBancaria)
class ContaPoupanca extends ContaBancaria {
    constructor(agencia, numero, saldo) {
        super(agencia, numero, "Conta Poupança", saldo);
    }
}

// Classe ContaUniversitaria (Herda de ContaBancaria)
class ContaUniversitaria extends ContaBancaria {
    constructor(agencia, numero, saldo) {
        super(agencia, numero, "Conta Universitária", saldo);
    }

    sacar(valor) {
        if (valor <= 500 && valor <= this.saldo) {
            this.saldo -= valor;
            return true;
        }
        return false;
    }
}

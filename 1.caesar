#!/usr/bin/env python
# -*- coding: utf-8 -*-
class Caesar():
    key = 'aáàạảãăắằặẳẵâấầậẩẫbcdđeéẹẻẽêếềệểễfghiíìịỉĩjklmnoóòọỏõôốồộổỗơớờợởỡpqrstuúùụủũưứừựửữvwxyýỳỵỷỹAÁÀẠẢÃĂẮẰẶẲẴÂẤẦẬẨẪBCDĐEÉẸẺẼÊẾỀỆỂỄFGHIÍÌỊỈĨJKLMNOÓÒỌỎÕÔỐỒỘỔỖƠỚỜỢỞỠPQRSTUÚÙỤỦŨƯỨỪỰỬỮVWXYÝỲỴỶỸ0123456789`~!@#$%^&*()'

    def encrypt(self, n, plaintext):
        """Encrypt the string and return the ciphertext"""
        result = ''

        for l in plaintext:
            try:
                i = (self.key.index(l) + n) % len(self.key)
                result += self.key[i]
            except ValueError:
                result += l
        return result


    def decrypt(self, n, ciphertext):
        """Decrypt the string and return the plaintext"""
        result = ''

        for l in ciphertext:
            try:
                i = (self.key.index(l) - n) % len(self.key)
                result += self.key[i]
            except ValueError:
                result += l

        return result


    def show_result(self, plaintext, n):
        """Generate a resulting cipher with elements shown"""
        encrypted = self.encrypt(n, plaintext)
        decrypted = self.decrypt(n, encrypted)

        print('Rotation: ', n)
        print('Plaintext: ', plaintext)
        print('Encrytped: ', encrypted)
        print('Decrytped: ', decrypted)

if __name__ == '__main__':
    caesar = Caesar()
    caesar.show_result("Xin Chào Việt Nam", 5)

---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/stop-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e1a4efc9709b7168e5de46ea0e19e2059f15243c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776646"
---
# <span data-ttu-id="a1253-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a1253-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a1253-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1253-102">SYNOPSIS</span></span>
<span data-ttu-id="a1253-103">Cancela uma operação de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a1253-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="a1253-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1253-104">SYNTAX</span></span>

```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1253-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1253-105">DESCRIPTION</span></span>
<span data-ttu-id="a1253-106">O cmdlet **Stop-AzKeyVaultCertificateOperation** cancela uma operação de certificado no serviço de compartimento de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1253-106">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="a1253-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1253-107">EXAMPLES</span></span>

### <span data-ttu-id="a1253-108">Exemplo 1: cancelar uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="a1253-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="a1253-109">Esse comando cancela a operação de certificado TestCert02.</span><span class="sxs-lookup"><span data-stu-id="a1253-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="a1253-110">OS</span><span class="sxs-lookup"><span data-stu-id="a1253-110">PARAMETERS</span></span>

### <span data-ttu-id="a1253-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1253-111">-DefaultProfile</span></span>
<span data-ttu-id="a1253-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1253-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a1253-113">-Force</span></span>
<span data-ttu-id="a1253-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1253-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1253-115">-Name</span></span>
<span data-ttu-id="a1253-116">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a1253-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-117">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a1253-117">-VaultName</span></span>
<span data-ttu-id="a1253-118">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a1253-118">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1253-119">-Confirm</span></span>
<span data-ttu-id="a1253-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1253-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1253-121">-WhatIf</span></span>
<span data-ttu-id="a1253-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1253-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1253-123">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1253-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1253-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1253-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1253-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1253-125">CommonParameters</span></span>
<span data-ttu-id="a1253-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1253-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1253-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1253-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1253-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1253-128">INPUTS</span></span>

### <span data-ttu-id="a1253-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1253-129">None</span></span>
<span data-ttu-id="a1253-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a1253-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1253-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1253-131">OUTPUTS</span></span>

### <span data-ttu-id="a1253-132">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a1253-132">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a1253-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1253-133">NOTES</span></span>

## <span data-ttu-id="a1253-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1253-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1253-135">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a1253-135">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="a1253-136">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a1253-136">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)


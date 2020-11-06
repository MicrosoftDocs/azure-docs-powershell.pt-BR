---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: b8a195ed5c11aa7782450c60f5915f2c3988ef3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429518"
---
# <span data-ttu-id="a6c28-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a6c28-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a6c28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6c28-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c28-103">Cancela uma operação de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a6c28-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6c28-104">SYNTAX</span></span>

### <span data-ttu-id="a6c28-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6c28-105">Default (Default)</span></span>
```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c28-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c28-106">InputObject</span></span>
```
Stop-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c28-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6c28-107">DESCRIPTION</span></span>
<span data-ttu-id="a6c28-108">O cmdlet **Stop-AzureKeyVaultCertificateOperation** cancela uma operação de certificado no serviço de compartimento de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c28-108">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="a6c28-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6c28-109">EXAMPLES</span></span>

### <span data-ttu-id="a6c28-110">Exemplo 1: cancelar uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="a6c28-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="a6c28-111">Esse comando cancela a operação de certificado TestCert02.</span><span class="sxs-lookup"><span data-stu-id="a6c28-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="a6c28-112">OS</span><span class="sxs-lookup"><span data-stu-id="a6c28-112">PARAMETERS</span></span>

### <span data-ttu-id="a6c28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c28-113">-DefaultProfile</span></span>
<span data-ttu-id="a6c28-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6c28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6c28-115">-Force</span></span>
<span data-ttu-id="a6c28-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6c28-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c28-117">-InputObject</span></span>
<span data-ttu-id="a6c28-118">Objeto Operation</span><span class="sxs-lookup"><span data-stu-id="a6c28-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6c28-119">-Name</span></span>
<span data-ttu-id="a6c28-120">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a6c28-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a6c28-121">-VaultName</span></span>
<span data-ttu-id="a6c28-122">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a6c28-122">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6c28-123">-Confirm</span></span>
<span data-ttu-id="a6c28-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c28-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c28-125">-WhatIf</span></span>
<span data-ttu-id="a6c28-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6c28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c28-127">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6c28-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c28-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6c28-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c28-129">CommonParameters</span></span>
<span data-ttu-id="a6c28-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c28-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c28-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c28-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6c28-132">INPUTS</span></span>

### <span data-ttu-id="a6c28-133">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a6c28-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>
<span data-ttu-id="a6c28-134">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6c28-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a6c28-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6c28-135">OUTPUTS</span></span>

### <span data-ttu-id="a6c28-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a6c28-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a6c28-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6c28-137">NOTES</span></span>

## <span data-ttu-id="a6c28-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6c28-138">RELATED LINKS</span></span>

[<span data-ttu-id="a6c28-139">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a6c28-139">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="a6c28-140">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a6c28-140">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)


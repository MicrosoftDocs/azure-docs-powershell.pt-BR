---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941878"
---
# <span data-ttu-id="24193-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="24193-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="24193-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24193-102">SYNOPSIS</span></span>
<span data-ttu-id="24193-103">Cancela uma operação de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24193-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="24193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24193-104">SYNTAX</span></span>

### <span data-ttu-id="24193-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="24193-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24193-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24193-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24193-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24193-107">DESCRIPTION</span></span>
<span data-ttu-id="24193-108">O cmdlet **Stop-AzKeyVaultCertificateOperation** cancela uma operação de certificado no serviço de compartimento de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="24193-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="24193-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24193-109">EXAMPLES</span></span>

### <span data-ttu-id="24193-110">Exemplo 1: cancelar uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="24193-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="24193-111">Esse comando cancela a operação de certificado TestCert02.</span><span class="sxs-lookup"><span data-stu-id="24193-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="24193-112">OS</span><span class="sxs-lookup"><span data-stu-id="24193-112">PARAMETERS</span></span>

### <span data-ttu-id="24193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24193-113">-DefaultProfile</span></span>
<span data-ttu-id="24193-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="24193-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24193-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24193-115">-Force</span></span>
<span data-ttu-id="24193-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="24193-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24193-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24193-117">-InputObject</span></span>
<span data-ttu-id="24193-118">Objeto Operation</span><span class="sxs-lookup"><span data-stu-id="24193-118">Operation object</span></span>

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

### <span data-ttu-id="24193-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="24193-119">-Name</span></span>
<span data-ttu-id="24193-120">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="24193-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="24193-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="24193-121">-VaultName</span></span>
<span data-ttu-id="24193-122">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="24193-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="24193-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24193-123">-Confirm</span></span>
<span data-ttu-id="24193-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24193-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24193-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24193-125">-WhatIf</span></span>
<span data-ttu-id="24193-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24193-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24193-127">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24193-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24193-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24193-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24193-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24193-129">CommonParameters</span></span>
<span data-ttu-id="24193-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24193-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24193-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24193-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24193-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24193-132">INPUTS</span></span>

### <span data-ttu-id="24193-133">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="24193-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="24193-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24193-134">OUTPUTS</span></span>

### <span data-ttu-id="24193-135">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="24193-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="24193-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24193-136">NOTES</span></span>

## <span data-ttu-id="24193-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24193-137">RELATED LINKS</span></span>

[<span data-ttu-id="24193-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="24193-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="24193-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="24193-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)


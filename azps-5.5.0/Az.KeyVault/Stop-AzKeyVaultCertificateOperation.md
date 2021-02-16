---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113083"
---
# <span data-ttu-id="529aa-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="529aa-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="529aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="529aa-102">SYNOPSIS</span></span>
<span data-ttu-id="529aa-103">Cancela uma operação de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="529aa-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="529aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="529aa-104">SYNTAX</span></span>

### <span data-ttu-id="529aa-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="529aa-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529aa-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="529aa-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529aa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="529aa-107">DESCRIPTION</span></span>
<span data-ttu-id="529aa-108">O cmdlet **Stop-AzKeyVaultCertificateOperation** cancela uma operação de certificado no serviço do Cofre de Chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="529aa-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="529aa-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="529aa-109">EXAMPLES</span></span>

### <span data-ttu-id="529aa-110">Exemplo 1: Cancelar uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="529aa-110">Example 1: Cancel a certificate operation</span></span>
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

<span data-ttu-id="529aa-111">Esse comando cancela a operação de certificado TestCert02.</span><span class="sxs-lookup"><span data-stu-id="529aa-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="529aa-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="529aa-112">PARAMETERS</span></span>

### <span data-ttu-id="529aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529aa-113">-DefaultProfile</span></span>
<span data-ttu-id="529aa-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="529aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="529aa-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="529aa-115">-Force</span></span>
<span data-ttu-id="529aa-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="529aa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="529aa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="529aa-117">-InputObject</span></span>
<span data-ttu-id="529aa-118">Objeto operation</span><span class="sxs-lookup"><span data-stu-id="529aa-118">Operation object</span></span>

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

### <span data-ttu-id="529aa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="529aa-119">-Name</span></span>
<span data-ttu-id="529aa-120">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="529aa-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="529aa-121">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="529aa-121">-VaultName</span></span>
<span data-ttu-id="529aa-122">Especifica o nome de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="529aa-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="529aa-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="529aa-123">-Confirm</span></span>
<span data-ttu-id="529aa-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529aa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="529aa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529aa-125">-WhatIf</span></span>
<span data-ttu-id="529aa-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="529aa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="529aa-127">O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="529aa-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="529aa-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="529aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="529aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529aa-129">CommonParameters</span></span>
<span data-ttu-id="529aa-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529aa-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="529aa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529aa-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="529aa-132">INPUTS</span></span>

### <span data-ttu-id="529aa-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="529aa-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="529aa-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="529aa-134">OUTPUTS</span></span>

### <span data-ttu-id="529aa-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="529aa-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="529aa-136">Notas</span><span class="sxs-lookup"><span data-stu-id="529aa-136">NOTES</span></span>

## <span data-ttu-id="529aa-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="529aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="529aa-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="529aa-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="529aa-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="529aa-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)


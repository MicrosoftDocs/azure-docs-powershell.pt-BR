---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942550"
---
# <span data-ttu-id="b8ded-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8ded-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b8ded-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8ded-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ded-103">Exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b8ded-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="b8ded-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8ded-104">SYNTAX</span></span>

### <span data-ttu-id="b8ded-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8ded-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ded-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ded-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8ded-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8ded-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ded-108">O cmdlet **Remove-AzKeyVaultCertificateIssuer** exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b8ded-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="b8ded-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8ded-109">EXAMPLES</span></span>

### <span data-ttu-id="b8ded-110">Exemplo 1: remover um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="b8ded-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="b8ded-111">Esse comando Remove o emissor do certificado chamado TestIssuer01 do cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="b8ded-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b8ded-112">OS</span><span class="sxs-lookup"><span data-stu-id="b8ded-112">PARAMETERS</span></span>

### <span data-ttu-id="b8ded-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ded-113">-DefaultProfile</span></span>
<span data-ttu-id="b8ded-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b8ded-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8ded-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b8ded-115">-Force</span></span>
<span data-ttu-id="b8ded-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8ded-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8ded-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ded-117">-InputObject</span></span>
<span data-ttu-id="b8ded-118">Objeto emissor do certificado</span><span class="sxs-lookup"><span data-stu-id="b8ded-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ded-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8ded-119">-Name</span></span>
<span data-ttu-id="b8ded-120">Especifica o nome do emissor que será removido.</span><span class="sxs-lookup"><span data-stu-id="b8ded-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ded-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8ded-121">-PassThru</span></span>
<span data-ttu-id="b8ded-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b8ded-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b8ded-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b8ded-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b8ded-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="b8ded-124">-VaultName</span></span>
<span data-ttu-id="b8ded-125">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b8ded-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b8ded-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8ded-126">-Confirm</span></span>
<span data-ttu-id="b8ded-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8ded-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ded-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ded-128">-WhatIf</span></span>
<span data-ttu-id="b8ded-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8ded-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8ded-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8ded-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8ded-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8ded-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ded-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ded-132">CommonParameters</span></span>
<span data-ttu-id="b8ded-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ded-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ded-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ded-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ded-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8ded-135">INPUTS</span></span>

### <span data-ttu-id="b8ded-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b8ded-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="b8ded-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8ded-137">OUTPUTS</span></span>

### <span data-ttu-id="b8ded-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8ded-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b8ded-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8ded-139">NOTES</span></span>

## <span data-ttu-id="b8ded-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8ded-140">RELATED LINKS</span></span>

[<span data-ttu-id="b8ded-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8ded-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b8ded-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b8ded-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)



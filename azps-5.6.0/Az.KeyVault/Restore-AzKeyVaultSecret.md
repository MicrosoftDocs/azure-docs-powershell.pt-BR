---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 56f5279b1d3645717a29e392fd45599344515a29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888690"
---
# <span data-ttu-id="dd904-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="dd904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd904-102">SYNOPSIS</span></span>
<span data-ttu-id="dd904-103">Cria um segredo em um cofre de chaves a partir de um segredo de backup.</span><span class="sxs-lookup"><span data-stu-id="dd904-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="dd904-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dd904-104">SYNTAX</span></span>

### <span data-ttu-id="dd904-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dd904-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd904-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd904-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd904-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd904-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd904-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dd904-108">DESCRIPTION</span></span>
<span data-ttu-id="dd904-109">O cmdlet **Restore-AzKeyVaultSecret** cria um segredo no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="dd904-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="dd904-110">Esse segredo é uma réplica do segredo de backup no arquivo de entrada e tem o mesmo nome do segredo original.</span><span class="sxs-lookup"><span data-stu-id="dd904-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="dd904-111">Se o cofre de chaves já tiver um segredo com o mesmo nome, esse cmdlet falhará em vez de sobrescrever o segredo original.</span><span class="sxs-lookup"><span data-stu-id="dd904-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="dd904-112">Se o backup contiver várias versões de um segredo, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="dd904-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="dd904-113">O cofre de chaves em que você restaura o segredo pode ser diferente do cofre de chaves de onde você fez o backup do segredo.</span><span class="sxs-lookup"><span data-stu-id="dd904-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="dd904-114">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="dd904-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="dd904-115">Consulte o Centro de Confiança do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para geografias.</span><span class="sxs-lookup"><span data-stu-id="dd904-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="dd904-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd904-116">EXAMPLES</span></span>

### <span data-ttu-id="dd904-117">Exemplo 1: Restaurar um segredo de backup</span><span class="sxs-lookup"><span data-stu-id="dd904-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="dd904-118">Este comando restaura um segredo, incluindo todas as suas versões, do arquivo de backup chamado Backup.blob para o cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="dd904-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="dd904-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dd904-119">PARAMETERS</span></span>

### <span data-ttu-id="dd904-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd904-120">-DefaultProfile</span></span>
<span data-ttu-id="dd904-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dd904-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd904-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="dd904-122">-InputFile</span></span>
<span data-ttu-id="dd904-123">Especifica o arquivo de entrada que contém o backup do segredo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="dd904-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd904-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd904-124">-InputObject</span></span>
<span data-ttu-id="dd904-125">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd904-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd904-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd904-126">-ResourceId</span></span>
<span data-ttu-id="dd904-127">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd904-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd904-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dd904-128">-VaultName</span></span>
<span data-ttu-id="dd904-129">Especifica o nome do cofre de chaves no qual restaurar o segredo.</span><span class="sxs-lookup"><span data-stu-id="dd904-129">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd904-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd904-130">-Confirm</span></span>
<span data-ttu-id="dd904-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd904-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd904-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd904-132">-WhatIf</span></span>
<span data-ttu-id="dd904-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd904-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd904-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd904-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd904-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd904-135">CommonParameters</span></span>
<span data-ttu-id="dd904-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd904-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd904-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd904-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd904-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd904-138">INPUTS</span></span>

### <span data-ttu-id="dd904-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dd904-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="dd904-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dd904-140">System.String</span></span>

## <span data-ttu-id="dd904-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dd904-141">OUTPUTS</span></span>

### <span data-ttu-id="dd904-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="dd904-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="dd904-143">NOTES</span></span>

## <span data-ttu-id="dd904-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd904-144">RELATED LINKS</span></span>

[<span data-ttu-id="dd904-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="dd904-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="dd904-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="dd904-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd904-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


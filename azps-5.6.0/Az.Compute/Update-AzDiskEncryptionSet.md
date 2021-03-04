---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 2567d43220193e9233322fbf8715f7b7698890b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889295"
---
# <span data-ttu-id="592e7-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="592e7-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="592e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592e7-102">SYNOPSIS</span></span>
<span data-ttu-id="592e7-103">Atualiza um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="592e7-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="592e7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="592e7-104">SYNTAX</span></span>

### <span data-ttu-id="592e7-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="592e7-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="592e7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="592e7-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="592e7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="592e7-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="592e7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="592e7-108">DESCRIPTION</span></span>
<span data-ttu-id="592e7-109">Atualiza um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="592e7-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="592e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="592e7-110">EXAMPLES</span></span>

### <span data-ttu-id="592e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="592e7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="592e7-112">Atualiza o conjunto de criptografia de disco usando a chave ativa determinada no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="592e7-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="592e7-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="592e7-113">PARAMETERS</span></span>

### <span data-ttu-id="592e7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="592e7-114">-AsJob</span></span>
<span data-ttu-id="592e7-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="592e7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="592e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592e7-116">-DefaultProfile</span></span>
<span data-ttu-id="592e7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="592e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="592e7-118">-InputObject</span></span>
<span data-ttu-id="592e7-119">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="592e7-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="592e7-120">-KeyUrl</span></span>
<span data-ttu-id="592e7-121">Url apontando para a chave ativa em KeyVault</span><span class="sxs-lookup"><span data-stu-id="592e7-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="592e7-122">-Name</span></span>
<span data-ttu-id="592e7-123">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="592e7-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="592e7-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="592e7-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="592e7-126">-ResourceId</span></span>
<span data-ttu-id="592e7-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="592e7-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="592e7-128">-SourceVaultId</span></span>
<span data-ttu-id="592e7-129">ID de recurso do KeyVault que contém a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="592e7-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="592e7-130">-Tag</span></span>
<span data-ttu-id="592e7-131">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="592e7-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="592e7-132">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="592e7-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="592e7-133">-Confirm</span></span>
<span data-ttu-id="592e7-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592e7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592e7-135">-WhatIf</span></span>
<span data-ttu-id="592e7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="592e7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592e7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="592e7-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592e7-138">CommonParameters</span></span>
<span data-ttu-id="592e7-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592e7-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="592e7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592e7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="592e7-141">INPUTS</span></span>

### <span data-ttu-id="592e7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="592e7-142">System.String</span></span>

### <span data-ttu-id="592e7-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="592e7-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="592e7-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="592e7-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="592e7-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="592e7-145">OUTPUTS</span></span>

### <span data-ttu-id="592e7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="592e7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="592e7-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="592e7-147">NOTES</span></span>

## <span data-ttu-id="592e7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="592e7-148">RELATED LINKS</span></span>

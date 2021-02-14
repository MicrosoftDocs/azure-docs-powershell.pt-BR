---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111068"
---
# <span data-ttu-id="b4a8b-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4a8b-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="b4a8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a8b-103">Atualiza um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="b4a8b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4a8b-104">SYNTAX</span></span>

### <span data-ttu-id="b4a8b-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4a8b-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a8b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b4a8b-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a8b-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="b4a8b-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a8b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a8b-109">Atualiza um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="b4a8b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a8b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4a8b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="b4a8b-112">Atualiza o conjunto de criptografia de disco usando a chave ativa determinada no cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="b4a8b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4a8b-113">PARAMETERS</span></span>

### <span data-ttu-id="b4a8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4a8b-114">-AsJob</span></span>
<span data-ttu-id="b4a8b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4a8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4a8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a8b-116">-DefaultProfile</span></span>
<span data-ttu-id="b4a8b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a8b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a8b-118">-InputObject</span></span>
<span data-ttu-id="b4a8b-119">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="b4a8b-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="b4a8b-120">-KeyUrl</span></span>
<span data-ttu-id="b4a8b-121">URL apontando para a chave ativa no KeyVault</span><span class="sxs-lookup"><span data-stu-id="b4a8b-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="b4a8b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4a8b-122">-Name</span></span>
<span data-ttu-id="b4a8b-123">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="b4a8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4a8b-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4a8b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4a8b-126">-ResourceId</span></span>
<span data-ttu-id="b4a8b-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="b4a8b-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b4a8b-128">-SourceVaultId</span></span>
<span data-ttu-id="b4a8b-129">ID do recurso do KeyVault que contém a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="b4a8b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4a8b-130">-Tag</span></span>
<span data-ttu-id="b4a8b-131">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4a8b-132">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b4a8b-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4a8b-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4a8b-133">-Confirm</span></span>
<span data-ttu-id="b4a8b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a8b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a8b-135">-WhatIf</span></span>
<span data-ttu-id="b4a8b-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a8b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a8b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a8b-138">CommonParameters</span></span>
<span data-ttu-id="b4a8b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a8b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a8b-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a8b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a8b-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4a8b-141">INPUTS</span></span>

### <span data-ttu-id="b4a8b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b4a8b-142">System.String</span></span>

### <span data-ttu-id="b4a8b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4a8b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="b4a8b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4a8b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4a8b-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4a8b-145">OUTPUTS</span></span>

### <span data-ttu-id="b4a8b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b4a8b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="b4a8b-147">Notas</span><span class="sxs-lookup"><span data-stu-id="b4a8b-147">NOTES</span></span>

## <span data-ttu-id="b4a8b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4a8b-148">RELATED LINKS</span></span>

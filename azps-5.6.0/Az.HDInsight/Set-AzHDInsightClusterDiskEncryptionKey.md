---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: addf0e06a3df625bde5b46cc8089fc89ced832dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889470"
---
# <span data-ttu-id="25158-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="25158-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="25158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25158-102">SYNOPSIS</span></span>
<span data-ttu-id="25158-103">Gira a chave de criptografia de disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="25158-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="25158-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="25158-104">SYNTAX</span></span>

### <span data-ttu-id="25158-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25158-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25158-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25158-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25158-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25158-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25158-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="25158-108">DESCRIPTION</span></span>
<span data-ttu-id="25158-109">Gire a chave de criptografia de disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="25158-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="25158-110">Para essa operação, o cluster deve ter acesso à chave atual e à nova chave pretendido, caso contrário, a operação de tecla de rotação falhará.</span><span class="sxs-lookup"><span data-stu-id="25158-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="25158-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25158-111">EXAMPLES</span></span>

### <span data-ttu-id="25158-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25158-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="25158-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25158-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="25158-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="25158-114">PARAMETERS</span></span>

### <span data-ttu-id="25158-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25158-115">-DefaultProfile</span></span>
<span data-ttu-id="25158-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25158-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25158-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="25158-117">-EncryptionKeyName</span></span>
<span data-ttu-id="25158-118">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="25158-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25158-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="25158-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="25158-120">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="25158-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25158-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="25158-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="25158-122">Obtém ou define o uri do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="25158-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25158-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25158-123">-InputObject</span></span>
<span data-ttu-id="25158-124">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="25158-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25158-125">-Name</span><span class="sxs-lookup"><span data-stu-id="25158-125">-Name</span></span>
<span data-ttu-id="25158-126">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="25158-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25158-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25158-127">-ResourceGroupName</span></span>
<span data-ttu-id="25158-128">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25158-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25158-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25158-129">-ResourceId</span></span>
<span data-ttu-id="25158-130">Obtém ou define a id do recurso.</span><span class="sxs-lookup"><span data-stu-id="25158-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25158-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25158-131">-Confirm</span></span>
<span data-ttu-id="25158-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25158-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25158-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25158-133">-WhatIf</span></span>
<span data-ttu-id="25158-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25158-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25158-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25158-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25158-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25158-136">CommonParameters</span></span>
<span data-ttu-id="25158-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25158-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25158-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25158-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25158-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25158-139">INPUTS</span></span>

### <span data-ttu-id="25158-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="25158-140">None</span></span>

## <span data-ttu-id="25158-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="25158-141">OUTPUTS</span></span>

### <span data-ttu-id="25158-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="25158-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="25158-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="25158-143">NOTES</span></span>

## <span data-ttu-id="25158-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25158-144">RELATED LINKS</span></span>

[<span data-ttu-id="25158-145">Criptografia de disco de chave gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="25158-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/azure/hdinsight/disk-encryption)

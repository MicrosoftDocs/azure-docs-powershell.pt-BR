---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116765"
---
# <span data-ttu-id="bfc25-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bfc25-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="bfc25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc25-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc25-103">Gira a chave de criptografia de disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="bfc25-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="bfc25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc25-104">SYNTAX</span></span>

### <span data-ttu-id="bfc25-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bfc25-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc25-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc25-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc25-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc25-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc25-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfc25-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc25-109">Gire a chave de criptografia de disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="bfc25-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="bfc25-110">Para esta operação, o cluster deve ter acesso à chave atual e à nova chave pretendido, caso contrário, a operação de tecla de rotação falhará.</span><span class="sxs-lookup"><span data-stu-id="bfc25-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="bfc25-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfc25-111">EXAMPLES</span></span>

### <span data-ttu-id="bfc25-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfc25-112">Example 1</span></span>
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

### <span data-ttu-id="bfc25-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bfc25-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="bfc25-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc25-114">PARAMETERS</span></span>

### <span data-ttu-id="bfc25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc25-115">-DefaultProfile</span></span>
<span data-ttu-id="bfc25-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc25-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="bfc25-117">-EncryptionKeyName</span></span>
<span data-ttu-id="bfc25-118">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="bfc25-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="bfc25-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="bfc25-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="bfc25-120">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="bfc25-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="bfc25-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="bfc25-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="bfc25-122">Obtém ou define o uri do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="bfc25-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="bfc25-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfc25-123">-InputObject</span></span>
<span data-ttu-id="bfc25-124">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="bfc25-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="bfc25-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfc25-125">-Name</span></span>
<span data-ttu-id="bfc25-126">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfc25-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="bfc25-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc25-127">-ResourceGroupName</span></span>
<span data-ttu-id="bfc25-128">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfc25-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="bfc25-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc25-129">-ResourceId</span></span>
<span data-ttu-id="bfc25-130">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bfc25-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="bfc25-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bfc25-131">-Confirm</span></span>
<span data-ttu-id="bfc25-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc25-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc25-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc25-133">-WhatIf</span></span>
<span data-ttu-id="bfc25-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bfc25-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfc25-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfc25-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc25-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc25-136">CommonParameters</span></span>
<span data-ttu-id="bfc25-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc25-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc25-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfc25-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc25-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="bfc25-139">INPUTS</span></span>

### <span data-ttu-id="bfc25-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bfc25-140">None</span></span>

## <span data-ttu-id="bfc25-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="bfc25-141">OUTPUTS</span></span>

### <span data-ttu-id="bfc25-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="bfc25-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="bfc25-143">Notas</span><span class="sxs-lookup"><span data-stu-id="bfc25-143">NOTES</span></span>

## <span data-ttu-id="bfc25-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc25-144">RELATED LINKS</span></span>

[<span data-ttu-id="bfc25-145">Criptografia de disco de chave gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="bfc25-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280326"
---
# <span data-ttu-id="3b4f5-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3b4f5-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="3b4f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4f5-103">Gira a chave de criptografia do disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="3b4f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b4f5-104">SYNTAX</span></span>

### <span data-ttu-id="3b4f5-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b4f5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4f5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b4f5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b4f5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b4f5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b4f5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b4f5-108">DESCRIPTION</span></span>
<span data-ttu-id="3b4f5-109">Gire a chave de criptografia do disco do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="3b4f5-110">Para esta operação, o cluster deve ter acesso à chave atual e à nova chave pretendida, caso contrário, a operação de tecla de giro falhará.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="3b4f5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b4f5-111">EXAMPLES</span></span>

### <span data-ttu-id="3b4f5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b4f5-112">Example 1</span></span>
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

### <span data-ttu-id="3b4f5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3b4f5-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="3b4f5-114">OS</span><span class="sxs-lookup"><span data-stu-id="3b4f5-114">PARAMETERS</span></span>

### <span data-ttu-id="3b4f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4f5-115">-DefaultProfile</span></span>
<span data-ttu-id="3b4f5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b4f5-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="3b4f5-117">-EncryptionKeyName</span></span>
<span data-ttu-id="3b4f5-118">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="3b4f5-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3b4f5-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="3b4f5-120">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="3b4f5-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="3b4f5-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="3b4f5-122">Obtém ou define o URI do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="3b4f5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b4f5-123">-InputObject</span></span>
<span data-ttu-id="3b4f5-124">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="3b4f5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b4f5-125">-Name</span></span>
<span data-ttu-id="3b4f5-126">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="3b4f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b4f5-128">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="3b4f5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b4f5-129">-ResourceId</span></span>
<span data-ttu-id="3b4f5-130">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="3b4f5-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b4f5-131">-Confirm</span></span>
<span data-ttu-id="3b4f5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b4f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4f5-133">-WhatIf</span></span>
<span data-ttu-id="3b4f5-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b4f5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b4f5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4f5-136">CommonParameters</span></span>
<span data-ttu-id="3b4f5-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4f5-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b4f5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4f5-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b4f5-139">INPUTS</span></span>

### <span data-ttu-id="3b4f5-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3b4f5-140">None</span></span>

## <span data-ttu-id="3b4f5-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b4f5-141">OUTPUTS</span></span>

### <span data-ttu-id="3b4f5-142">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="3b4f5-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="3b4f5-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b4f5-143">NOTES</span></span>

## <span data-ttu-id="3b4f5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b4f5-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b4f5-145">Criptografia de disco da chave gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="3b4f5-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)

---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945962"
---
# <span data-ttu-id="5c14b-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="5c14b-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="5c14b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c14b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c14b-103">Define o número de nós de dados para um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5c14b-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="5c14b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c14b-104">SYNTAX</span></span>

### <span data-ttu-id="5c14b-105">Defina o tamanho do cluster em nós com nome.</span><span class="sxs-lookup"><span data-stu-id="5c14b-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c14b-106">Defina o tamanho do cluster em nós com cluster do pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c14b-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5c14b-107">Cluster por nome (com credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="5c14b-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c14b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c14b-108">DESCRIPTION</span></span>
<span data-ttu-id="5c14b-109">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="5c14b-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="5c14b-110">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="5c14b-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="5c14b-111">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5c14b-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="5c14b-112">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="5c14b-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="5c14b-113">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="5c14b-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="5c14b-114">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5c14b-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="5c14b-115">O cmdlet **set-AzureHDInsightClusterSize** define o número de nós de dados de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5c14b-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5c14b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c14b-116">EXAMPLES</span></span>

## <span data-ttu-id="5c14b-117">OS</span><span class="sxs-lookup"><span data-stu-id="5c14b-117">PARAMETERS</span></span>

### <span data-ttu-id="5c14b-118">-Certificado</span><span class="sxs-lookup"><span data-stu-id="5c14b-118">-Certificate</span></span>
<span data-ttu-id="5c14b-119">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c14b-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="5c14b-120">-Cluster</span></span>
<span data-ttu-id="5c14b-121">Especifica o cluster a ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="5c14b-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="5c14b-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="5c14b-123">Especifica o número de nós de dados a serem criados para um cluster.</span><span class="sxs-lookup"><span data-stu-id="5c14b-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-124">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="5c14b-124">-Endpoint</span></span>
<span data-ttu-id="5c14b-125">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="5c14b-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="5c14b-126">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="5c14b-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5c14b-127">-Force</span></span>
<span data-ttu-id="5c14b-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c14b-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="5c14b-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="5c14b-130">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="5c14b-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c14b-131">-Name</span></span>
<span data-ttu-id="5c14b-132">Especifica o nome do cluster HDInsight a ser redimensionado.</span><span class="sxs-lookup"><span data-stu-id="5c14b-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5c14b-133">-Profile</span></span>
<span data-ttu-id="5c14b-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5c14b-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c14b-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5c14b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-136">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="5c14b-136">-Subscription</span></span>
<span data-ttu-id="5c14b-137">Especifica uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c14b-137">Specifies a subscription.</span></span>
<span data-ttu-id="5c14b-138">Esse cmdlet define o tamanho do cluster para a assinatura que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5c14b-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c14b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c14b-139">CommonParameters</span></span>
<span data-ttu-id="5c14b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c14b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c14b-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c14b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c14b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c14b-142">INPUTS</span></span>

## <span data-ttu-id="5c14b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c14b-143">OUTPUTS</span></span>

## <span data-ttu-id="5c14b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c14b-144">NOTES</span></span>

## <span data-ttu-id="5c14b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c14b-145">RELATED LINKS</span></span>


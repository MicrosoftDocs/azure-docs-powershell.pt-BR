---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946476"
---
# <span data-ttu-id="89b85-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="89b85-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="89b85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89b85-102">SYNOPSIS</span></span>
<span data-ttu-id="89b85-103">Exclui um cluster HDInsight de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="89b85-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="89b85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89b85-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="89b85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89b85-105">DESCRIPTION</span></span>
<span data-ttu-id="89b85-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="89b85-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="89b85-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="89b85-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="89b85-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="89b85-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="89b85-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="89b85-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="89b85-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="89b85-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="89b85-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="89b85-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="89b85-112">O cmdlet **Remove-AzureHDInsightCluster** exclui o cluster de serviço HDInsight especificado de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="89b85-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="89b85-113">Essa operação também exclui todos os dados armazenados no Hadoop (sistema de arquivos distribuído) Hadoop no cluster.</span><span class="sxs-lookup"><span data-stu-id="89b85-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="89b85-114">Os dados armazenados na conta de armazenamento associada ao Azure não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="89b85-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="89b85-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89b85-115">EXAMPLES</span></span>

### <span data-ttu-id="89b85-116">Exemplo 1: remover um cluster</span><span class="sxs-lookup"><span data-stu-id="89b85-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="89b85-117">Esse comando exclui o cluster HDInsight chamado HDICluster.</span><span class="sxs-lookup"><span data-stu-id="89b85-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="89b85-118">OS</span><span class="sxs-lookup"><span data-stu-id="89b85-118">PARAMETERS</span></span>

### <span data-ttu-id="89b85-119">-Certificado</span><span class="sxs-lookup"><span data-stu-id="89b85-119">-Certificate</span></span>
<span data-ttu-id="89b85-120">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="89b85-120">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-121">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="89b85-121">-Endpoint</span></span>
<span data-ttu-id="89b85-122">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="89b85-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="89b85-123">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="89b85-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="89b85-124">-HostedService</span></span>
<span data-ttu-id="89b85-125">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="89b85-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="89b85-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="89b85-127">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="89b85-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="89b85-128">-Name</span></span>
<span data-ttu-id="89b85-129">Especifica o nome do cluster HDInsight a ser removido.</span><span class="sxs-lookup"><span data-stu-id="89b85-129">Specifies the name of the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="89b85-130">-Profile</span></span>
<span data-ttu-id="89b85-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="89b85-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89b85-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="89b85-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89b85-133">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="89b85-133">-Subscription</span></span>
<span data-ttu-id="89b85-134">Especifica a conta de assinatura que contém o cluster HDInsight a ser removida.</span><span class="sxs-lookup"><span data-stu-id="89b85-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b85-135">CommonParameters</span></span>
<span data-ttu-id="89b85-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b85-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b85-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b85-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89b85-138">INPUTS</span></span>

## <span data-ttu-id="89b85-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89b85-139">OUTPUTS</span></span>

## <span data-ttu-id="89b85-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89b85-140">NOTES</span></span>

## <span data-ttu-id="89b85-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89b85-141">RELATED LINKS</span></span>

[<span data-ttu-id="89b85-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="89b85-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="89b85-143">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="89b85-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="89b85-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="89b85-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)



---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945837"
---
# <span data-ttu-id="93ac3-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="93ac3-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="93ac3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="93ac3-103">Seleciona um cluster HDInsight para o cmdlet Invoke-AzureHDInsightHiveJob usar para enviar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="93ac3-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="93ac3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93ac3-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93ac3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="93ac3-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="93ac3-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="93ac3-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="93ac3-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="93ac3-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93ac3-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="93ac3-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="93ac3-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="93ac3-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="93ac3-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="93ac3-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="93ac3-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="93ac3-112">O cmdlet **use-AzureHDInsightCluster** seleciona o cluster do Azure HDInsight para o cmdlet **Invoke-AzureHDInsightHiveJob** ser usado para enviar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="93ac3-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="93ac3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93ac3-113">EXAMPLES</span></span>

## <span data-ttu-id="93ac3-114">OS</span><span class="sxs-lookup"><span data-stu-id="93ac3-114">PARAMETERS</span></span>

### <span data-ttu-id="93ac3-115">-Certificado</span><span class="sxs-lookup"><span data-stu-id="93ac3-115">-Certificate</span></span>
<span data-ttu-id="93ac3-116">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="93ac3-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="93ac3-117">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="93ac3-117">-Endpoint</span></span>
<span data-ttu-id="93ac3-118">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="93ac3-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="93ac3-119">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="93ac3-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="93ac3-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="93ac3-120">-HostedService</span></span>
<span data-ttu-id="93ac3-121">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93ac3-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="93ac3-122">Se você não especificar esse parâmetro, o namespace padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="93ac3-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="93ac3-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="93ac3-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="93ac3-124">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="93ac3-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="93ac3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="93ac3-125">-Name</span></span>
<span data-ttu-id="93ac3-126">Especifica o nome do cluster que é usado pelo cmdlet **Invoke-AzureHDInsightHiveJob** .</span><span class="sxs-lookup"><span data-stu-id="93ac3-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="93ac3-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="93ac3-127">-Profile</span></span>
<span data-ttu-id="93ac3-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="93ac3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93ac3-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="93ac3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93ac3-130">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="93ac3-130">-Subscription</span></span>
<span data-ttu-id="93ac3-131">Especifica a assinatura que contém os clusters HDInsight a serem usados.</span><span class="sxs-lookup"><span data-stu-id="93ac3-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="93ac3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ac3-132">CommonParameters</span></span>
<span data-ttu-id="93ac3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ac3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ac3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ac3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ac3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93ac3-135">INPUTS</span></span>

## <span data-ttu-id="93ac3-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93ac3-136">OUTPUTS</span></span>

## <span data-ttu-id="93ac3-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93ac3-137">NOTES</span></span>

## <span data-ttu-id="93ac3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93ac3-138">RELATED LINKS</span></span>

[<span data-ttu-id="93ac3-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="93ac3-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="93ac3-140">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="93ac3-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="93ac3-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="93ac3-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)



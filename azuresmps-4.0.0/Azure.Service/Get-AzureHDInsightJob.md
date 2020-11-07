---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946350"
---
# <span data-ttu-id="f7297-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7297-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="f7297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7297-102">SYNOPSIS</span></span>
<span data-ttu-id="f7297-103">Obtém trabalhos HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7297-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="f7297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7297-104">SYNTAX</span></span>

### <span data-ttu-id="f7297-105">Obter jobDetails histórico de um cluster HDInsight (padrão)</span><span class="sxs-lookup"><span data-stu-id="f7297-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f7297-106">Obter o histórico jobDetails de um cluster HDInsight (com uma credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="f7297-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f7297-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7297-107">DESCRIPTION</span></span>
<span data-ttu-id="f7297-108">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="f7297-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f7297-109">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="f7297-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f7297-110">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7297-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f7297-111">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f7297-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f7297-112">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f7297-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f7297-113">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f7297-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f7297-114">O cmdlet **Get-AzureHDInsightJob** Obtém trabalhos recentes do Azure HDInsight para um cluster especificado e os exibe em ordem cronológica inversa.</span><span class="sxs-lookup"><span data-stu-id="f7297-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="f7297-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7297-115">EXAMPLES</span></span>

## <span data-ttu-id="f7297-116">OS</span><span class="sxs-lookup"><span data-stu-id="f7297-116">PARAMETERS</span></span>

### <span data-ttu-id="f7297-117">-Certificado</span><span class="sxs-lookup"><span data-stu-id="f7297-117">-Certificate</span></span>
<span data-ttu-id="f7297-118">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7297-118">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="f7297-119">-Cluster</span></span>
<span data-ttu-id="f7297-120">Especifica um cluster.</span><span class="sxs-lookup"><span data-stu-id="f7297-120">Specifies a cluster.</span></span>
<span data-ttu-id="f7297-121">Esse cmdlet obtém trabalhos HDInsight que são executados no cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f7297-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="f7297-122">-Credential</span></span>
<span data-ttu-id="f7297-123">Especifica as credenciais a serem usadas para acesso HTTP direto a um cluster.</span><span class="sxs-lookup"><span data-stu-id="f7297-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="f7297-124">Você pode especificar esse parâmetro em vez do parâmetro de *assinatura* para autenticar o acesso a um cluster.</span><span class="sxs-lookup"><span data-stu-id="f7297-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-125">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="f7297-125">-Endpoint</span></span>
<span data-ttu-id="f7297-126">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="f7297-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f7297-127">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="f7297-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f7297-128">-HostedService</span></span>
<span data-ttu-id="f7297-129">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="f7297-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f7297-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="f7297-131">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="f7297-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="f7297-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="f7297-132">-JobId</span></span>
<span data-ttu-id="f7297-133">Especifica a ID de um trabalho a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="f7297-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f7297-134">-Profile</span></span>
<span data-ttu-id="f7297-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f7297-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f7297-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f7297-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7297-137">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f7297-137">-Subscription</span></span>
<span data-ttu-id="f7297-138">Especifica a assinatura que contém os trabalhos HDInsight a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="f7297-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7297-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7297-139">CommonParameters</span></span>
<span data-ttu-id="f7297-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7297-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7297-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7297-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7297-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7297-142">INPUTS</span></span>

## <span data-ttu-id="f7297-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7297-143">OUTPUTS</span></span>

## <span data-ttu-id="f7297-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7297-144">NOTES</span></span>

## <span data-ttu-id="f7297-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7297-145">RELATED LINKS</span></span>

[<span data-ttu-id="f7297-146">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7297-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="f7297-147">Parar-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7297-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="f7297-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7297-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)



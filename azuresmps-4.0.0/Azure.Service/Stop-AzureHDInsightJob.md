---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945764"
---
# <span data-ttu-id="322da-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="322da-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="322da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="322da-102">SYNOPSIS</span></span>
<span data-ttu-id="322da-103">Interrompe um trabalho do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="322da-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="322da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="322da-104">SYNTAX</span></span>

### <span data-ttu-id="322da-105">Iniciar o jobDetails em um cluster HDInsight (padrão)</span><span class="sxs-lookup"><span data-stu-id="322da-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="322da-106">Iniciar o jobDetails em um cluster HDInsight (com uma credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="322da-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="322da-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="322da-107">DESCRIPTION</span></span>
<span data-ttu-id="322da-108">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="322da-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="322da-109">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="322da-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="322da-110">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="322da-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="322da-111">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="322da-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="322da-112">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="322da-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="322da-113">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="322da-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="322da-114">O cmdlet **Stop-AzureHDInsightJob** interrompe um trabalho do Azure HDInsight no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="322da-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="322da-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="322da-115">EXAMPLES</span></span>

## <span data-ttu-id="322da-116">OS</span><span class="sxs-lookup"><span data-stu-id="322da-116">PARAMETERS</span></span>

### <span data-ttu-id="322da-117">-Certificado</span><span class="sxs-lookup"><span data-stu-id="322da-117">-Certificate</span></span>
<span data-ttu-id="322da-118">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="322da-118">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="322da-119">-Cluster</span></span>
<span data-ttu-id="322da-120">Especifica um cluster.</span><span class="sxs-lookup"><span data-stu-id="322da-120">Specifies a cluster.</span></span>
<span data-ttu-id="322da-121">Esse cmdlet interrompe um trabalho que é executado no cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="322da-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322da-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="322da-122">-Credential</span></span>
<span data-ttu-id="322da-123">Especifica as credenciais a serem usadas para acesso HTTP direto a um cluster.</span><span class="sxs-lookup"><span data-stu-id="322da-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="322da-124">Você pode especificar esse parâmetro em vez do parâmetro de *assinatura* para autenticar o acesso a um cluster.</span><span class="sxs-lookup"><span data-stu-id="322da-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-125">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="322da-125">-Endpoint</span></span>
<span data-ttu-id="322da-126">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="322da-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="322da-127">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="322da-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="322da-128">-HostedService</span></span>
<span data-ttu-id="322da-129">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="322da-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="322da-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="322da-131">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="322da-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="322da-132">-JobId</span></span>
<span data-ttu-id="322da-133">Especifica a ID do trabalho HDInsight a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="322da-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322da-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="322da-134">-Profile</span></span>
<span data-ttu-id="322da-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="322da-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="322da-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="322da-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="322da-137">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="322da-137">-Subscription</span></span>
<span data-ttu-id="322da-138">Especifica uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="322da-138">Specifies a subscription.</span></span>
<span data-ttu-id="322da-139">Esse cmdlet interrompe um trabalho para a assinatura que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="322da-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322da-140">CommonParameters</span></span>
<span data-ttu-id="322da-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="322da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322da-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322da-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322da-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="322da-143">INPUTS</span></span>

## <span data-ttu-id="322da-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="322da-144">OUTPUTS</span></span>

## <span data-ttu-id="322da-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="322da-145">NOTES</span></span>

## <span data-ttu-id="322da-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="322da-146">RELATED LINKS</span></span>

[<span data-ttu-id="322da-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="322da-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="322da-148">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="322da-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="322da-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="322da-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)



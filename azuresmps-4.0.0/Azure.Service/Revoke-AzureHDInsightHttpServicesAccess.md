---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946434"
---
# <span data-ttu-id="65dfa-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="65dfa-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="65dfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="65dfa-103">Desabilita o acesso HTTP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="65dfa-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="65dfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65dfa-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65dfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="65dfa-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="65dfa-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="65dfa-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="65dfa-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="65dfa-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="65dfa-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="65dfa-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="65dfa-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="65dfa-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="65dfa-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="65dfa-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="65dfa-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="65dfa-112">O cmdlet **REVOKE-AzureHDInsightHttpServicesAccess** desabilita o acesso http a um cluster para os serviços Web ODBC, Ambari, Oozie e WebHCatalog.</span><span class="sxs-lookup"><span data-stu-id="65dfa-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="65dfa-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65dfa-113">EXAMPLES</span></span>

## <span data-ttu-id="65dfa-114">OS</span><span class="sxs-lookup"><span data-stu-id="65dfa-114">PARAMETERS</span></span>

### <span data-ttu-id="65dfa-115">-Certificado</span><span class="sxs-lookup"><span data-stu-id="65dfa-115">-Certificate</span></span>
<span data-ttu-id="65dfa-116">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="65dfa-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="65dfa-117">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="65dfa-117">-Endpoint</span></span>
<span data-ttu-id="65dfa-118">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="65dfa-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="65dfa-119">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="65dfa-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="65dfa-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="65dfa-120">-HostedService</span></span>
<span data-ttu-id="65dfa-121">Especifica o namespace de um serviço HDInsight se você não quiser usar o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="65dfa-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="65dfa-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="65dfa-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="65dfa-123">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="65dfa-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="65dfa-124">-Local</span><span class="sxs-lookup"><span data-stu-id="65dfa-124">-Location</span></span>
<span data-ttu-id="65dfa-125">Especifica a região em que um cluster HDInsight está localizado.</span><span class="sxs-lookup"><span data-stu-id="65dfa-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dfa-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="65dfa-126">-Name</span></span>
<span data-ttu-id="65dfa-127">Especifica o nome de um cluster.</span><span class="sxs-lookup"><span data-stu-id="65dfa-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="65dfa-128">Esse cmdlet desabilita o acesso HTTP ao cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="65dfa-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="65dfa-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="65dfa-129">-Profile</span></span>
<span data-ttu-id="65dfa-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="65dfa-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65dfa-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="65dfa-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65dfa-132">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="65dfa-132">-Subscription</span></span>
<span data-ttu-id="65dfa-133">Especifica a conta de assinatura que contém o cluster HDInsight a revogar.</span><span class="sxs-lookup"><span data-stu-id="65dfa-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="65dfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dfa-134">CommonParameters</span></span>
<span data-ttu-id="65dfa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65dfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dfa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65dfa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dfa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65dfa-137">INPUTS</span></span>

## <span data-ttu-id="65dfa-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65dfa-138">OUTPUTS</span></span>

## <span data-ttu-id="65dfa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65dfa-139">NOTES</span></span>

## <span data-ttu-id="65dfa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65dfa-140">RELATED LINKS</span></span>

[<span data-ttu-id="65dfa-141">Grant AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="65dfa-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)



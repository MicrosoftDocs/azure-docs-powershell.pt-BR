---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946351"
---
# <span data-ttu-id="43331-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="43331-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="43331-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43331-102">SYNOPSIS</span></span>
<span data-ttu-id="43331-103">Obtém propriedades específicas para um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43331-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="43331-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43331-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="43331-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43331-105">DESCRIPTION</span></span>
<span data-ttu-id="43331-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="43331-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="43331-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="43331-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="43331-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43331-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="43331-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="43331-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="43331-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="43331-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="43331-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="43331-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="43331-112">O cmdlet **Get-AzureHDInsightProperties** Obtém propriedades específicas para um serviço do Azure HDInsight, como uma lista de regiões do Azure disponíveis, versões de cluster HDInsight e capacidade de computação disponível.</span><span class="sxs-lookup"><span data-stu-id="43331-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="43331-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43331-113">EXAMPLES</span></span>

### <span data-ttu-id="43331-114">Exemplo 1: obter as propriedades do HDInsight para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="43331-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="43331-115">O primeiro comando obtém o nome da assinatura atual do Azure e, em seguida, armazena-a na variável $SubName.</span><span class="sxs-lookup"><span data-stu-id="43331-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="43331-116">O segundo comando obtém as propriedades do HDInsight para a assinatura em $SubName.</span><span class="sxs-lookup"><span data-stu-id="43331-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="43331-117">OS</span><span class="sxs-lookup"><span data-stu-id="43331-117">PARAMETERS</span></span>

### <span data-ttu-id="43331-118">-Certificado</span><span class="sxs-lookup"><span data-stu-id="43331-118">-Certificate</span></span>
<span data-ttu-id="43331-119">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="43331-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="43331-120">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="43331-120">-Endpoint</span></span>
<span data-ttu-id="43331-121">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="43331-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="43331-122">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="43331-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="43331-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="43331-123">-HostedService</span></span>
<span data-ttu-id="43331-124">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43331-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="43331-125">Se você não especificar esse parâmetro, esse cmdlet usará o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="43331-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="43331-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="43331-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="43331-127">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="43331-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="43331-128">-Localizações</span><span class="sxs-lookup"><span data-stu-id="43331-128">-Locations</span></span>
<span data-ttu-id="43331-129">Indica que esse cmdlet obtém a lista de regiões do Azure onde o serviço HDInsight está disponível.</span><span class="sxs-lookup"><span data-stu-id="43331-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43331-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="43331-130">-Profile</span></span>
<span data-ttu-id="43331-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="43331-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43331-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="43331-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43331-133">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="43331-133">-Subscription</span></span>
<span data-ttu-id="43331-134">Especifica a assinatura que contém as propriedades do HDInsight a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="43331-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="43331-135">-Versões</span><span class="sxs-lookup"><span data-stu-id="43331-135">-Versions</span></span>
<span data-ttu-id="43331-136">Indica que esse cmdlet obtém a lista de versões de cluster HDInsight que estão disponíveis no serviço para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="43331-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43331-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43331-137">CommonParameters</span></span>
<span data-ttu-id="43331-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43331-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43331-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43331-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43331-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43331-140">INPUTS</span></span>

## <span data-ttu-id="43331-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43331-141">OUTPUTS</span></span>

## <span data-ttu-id="43331-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43331-142">NOTES</span></span>

## <span data-ttu-id="43331-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43331-143">RELATED LINKS</span></span>


---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945644"
---
# <span data-ttu-id="f0761-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f0761-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="f0761-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0761-102">SYNOPSIS</span></span>
<span data-ttu-id="f0761-103">Obtém um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f0761-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="f0761-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0761-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0761-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0761-105">DESCRIPTION</span></span>
<span data-ttu-id="f0761-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="f0761-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f0761-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="f0761-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f0761-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f0761-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f0761-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f0761-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f0761-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f0761-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f0761-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0761-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f0761-112">O cmdlet **Get-AzureHDInsightCluster** Obtém os clusters de serviço do Azure HDInsight para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f0761-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="f0761-113">Você pode usar o parâmetro *Name* para obter um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="f0761-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="f0761-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0761-114">EXAMPLES</span></span>

### <span data-ttu-id="f0761-115">Exemplo 1: obter os clusters em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="f0761-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="f0761-116">Esse comando obtém informações sobre os clusters HDInsight na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f0761-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="f0761-117">OS</span><span class="sxs-lookup"><span data-stu-id="f0761-117">PARAMETERS</span></span>

### <span data-ttu-id="f0761-118">-Certificado</span><span class="sxs-lookup"><span data-stu-id="f0761-118">-Certificate</span></span>
<span data-ttu-id="f0761-119">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0761-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="f0761-120">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="f0761-120">-Endpoint</span></span>
<span data-ttu-id="f0761-121">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="f0761-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f0761-122">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="f0761-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="f0761-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f0761-123">-HostedService</span></span>
<span data-ttu-id="f0761-124">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f0761-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="f0761-125">Se você não especificar esse parâmetro, esse cmdlet usará o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="f0761-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="f0761-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f0761-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="f0761-127">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="f0761-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="f0761-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0761-128">-Name</span></span>
<span data-ttu-id="f0761-129">Especifica o nome de um cluster HDInsight a obter.</span><span class="sxs-lookup"><span data-stu-id="f0761-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0761-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f0761-130">-Profile</span></span>
<span data-ttu-id="f0761-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f0761-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0761-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f0761-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0761-133">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="f0761-133">-Subscription</span></span>
<span data-ttu-id="f0761-134">Especifica a assinatura que contém o cluster HDInsight a obter.</span><span class="sxs-lookup"><span data-stu-id="f0761-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="f0761-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0761-135">CommonParameters</span></span>
<span data-ttu-id="f0761-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0761-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0761-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0761-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0761-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0761-138">INPUTS</span></span>

## <span data-ttu-id="f0761-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0761-139">OUTPUTS</span></span>

## <span data-ttu-id="f0761-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0761-140">NOTES</span></span>

## <span data-ttu-id="f0761-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0761-141">RELATED LINKS</span></span>

[<span data-ttu-id="f0761-142">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f0761-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="f0761-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f0761-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="f0761-144">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f0761-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)



---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946498"
---
# <span data-ttu-id="4f68f-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f68f-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="4f68f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f68f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f68f-103">Concede acesso HTTP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="4f68f-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="4f68f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f68f-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f68f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f68f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f68f-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="4f68f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4f68f-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="4f68f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4f68f-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f68f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4f68f-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4f68f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4f68f-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4f68f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4f68f-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f68f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4f68f-112">O cmdlet **Grant-AzureHDInsightHttpServicesAccess** concede acesso http a um cluster do Azure HDINSIGHT usando ODBC, Ambari, Oozie e Web Services.</span><span class="sxs-lookup"><span data-stu-id="4f68f-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="4f68f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f68f-113">EXAMPLES</span></span>

## <span data-ttu-id="4f68f-114">OS</span><span class="sxs-lookup"><span data-stu-id="4f68f-114">PARAMETERS</span></span>

### <span data-ttu-id="4f68f-115">-Certificado</span><span class="sxs-lookup"><span data-stu-id="4f68f-115">-Certificate</span></span>
<span data-ttu-id="4f68f-116">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f68f-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="4f68f-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="4f68f-117">-Credential</span></span>
<span data-ttu-id="4f68f-118">Especifica um nome de usuário e uma senha para acesso HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f68f-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f68f-119">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="4f68f-119">-Endpoint</span></span>
<span data-ttu-id="4f68f-120">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="4f68f-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4f68f-121">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="4f68f-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="4f68f-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4f68f-122">-HostedService</span></span>
<span data-ttu-id="4f68f-123">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f68f-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="4f68f-124">Se você não especificar esse parâmetro, esse cmdlet usará o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="4f68f-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="4f68f-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4f68f-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="4f68f-126">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="4f68f-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="4f68f-127">-Local</span><span class="sxs-lookup"><span data-stu-id="4f68f-127">-Location</span></span>
<span data-ttu-id="4f68f-128">Especifica a região do Azure na qual um cluster está localizado.</span><span class="sxs-lookup"><span data-stu-id="4f68f-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="4f68f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f68f-129">-Name</span></span>
<span data-ttu-id="4f68f-130">Especifica o nome de um cluster.</span><span class="sxs-lookup"><span data-stu-id="4f68f-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="4f68f-131">Esse cmdlet concede acesso HTTP ao cluster que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4f68f-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f68f-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4f68f-132">-Profile</span></span>
<span data-ttu-id="4f68f-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4f68f-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f68f-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4f68f-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f68f-135">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="4f68f-135">-Subscription</span></span>
<span data-ttu-id="4f68f-136">Especifica a assinatura que contém o cluster HDInsight para o qual conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="4f68f-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="4f68f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f68f-137">CommonParameters</span></span>
<span data-ttu-id="4f68f-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f68f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f68f-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f68f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f68f-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f68f-140">INPUTS</span></span>

## <span data-ttu-id="4f68f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f68f-141">OUTPUTS</span></span>

## <span data-ttu-id="4f68f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f68f-142">NOTES</span></span>

## <span data-ttu-id="4f68f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f68f-143">RELATED LINKS</span></span>

[<span data-ttu-id="4f68f-144">REVOKE-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4f68f-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)



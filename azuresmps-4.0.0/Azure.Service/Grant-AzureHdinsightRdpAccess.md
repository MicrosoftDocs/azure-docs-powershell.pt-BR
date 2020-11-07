---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946262"
---
# <span data-ttu-id="c3ed4-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="c3ed4-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="c3ed4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ed4-103">Concede acesso a RDP a um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="c3ed4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3ed4-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3ed4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ed4-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c3ed4-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c3ed4-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c3ed4-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c3ed4-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c3ed4-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c3ed4-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c3ed4-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c3ed4-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c3ed4-112">O cmdlet **Grant-AzureHDInsightRdpAccess** concede acesso ao protocolo RDP a um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c3ed4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3ed4-113">EXAMPLES</span></span>

## <span data-ttu-id="c3ed4-114">OS</span><span class="sxs-lookup"><span data-stu-id="c3ed4-114">PARAMETERS</span></span>

### <span data-ttu-id="c3ed4-115">-Certificado</span><span class="sxs-lookup"><span data-stu-id="c3ed4-115">-Certificate</span></span>
<span data-ttu-id="c3ed4-116">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="c3ed4-117">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="c3ed4-117">-Endpoint</span></span>
<span data-ttu-id="c3ed4-118">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c3ed4-119">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="c3ed4-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c3ed4-120">-HostedService</span></span>
<span data-ttu-id="c3ed4-121">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="c3ed4-122">Se você não especificar esse parâmetro, esse cmdlet usará o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="c3ed4-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c3ed4-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="c3ed4-124">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="c3ed4-125">-Local</span><span class="sxs-lookup"><span data-stu-id="c3ed4-125">-Location</span></span>
<span data-ttu-id="c3ed4-126">Especifica a região do Azure na qual um cluster está localizado.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="c3ed4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3ed4-127">-Name</span></span>
<span data-ttu-id="c3ed4-128">Especifica o nome de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="c3ed4-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c3ed4-129">-Profile</span></span>
<span data-ttu-id="c3ed4-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3ed4-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3ed4-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="c3ed4-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="c3ed4-133">Especifica a expiração, como um objeto **DateTime** , para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed4-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c3ed4-134">-RdpCredential</span></span>
<span data-ttu-id="c3ed4-135">Especifica as credenciais para o acesso RDP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-135">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="c3ed4-136">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="c3ed4-136">-Subscription</span></span>
<span data-ttu-id="c3ed4-137">Especifica a assinatura que contém o cluster HDInsight para o qual conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="c3ed4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ed4-138">CommonParameters</span></span>
<span data-ttu-id="c3ed4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ed4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ed4-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ed4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ed4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3ed4-141">INPUTS</span></span>

## <span data-ttu-id="c3ed4-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3ed4-142">OUTPUTS</span></span>

## <span data-ttu-id="c3ed4-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3ed4-143">NOTES</span></span>

## <span data-ttu-id="c3ed4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3ed4-144">RELATED LINKS</span></span>

[<span data-ttu-id="c3ed4-145">REVOKE-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="c3ed4-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)



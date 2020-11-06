---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 003072e6821561c78975d50fa627edf0f7fd120a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430284"
---
# <span data-ttu-id="3f14a-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3f14a-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="3f14a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f14a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f14a-103">Adiciona um objeto de segurança de um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="3f14a-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f14a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f14a-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f14a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f14a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f14a-106">O perfil de segurança é usado para criar um cluster seguro, kerberizing-lo.</span><span class="sxs-lookup"><span data-stu-id="3f14a-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="3f14a-107">O perfil de segurança contém a configuração relacionada à junção do cluster ao domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f14a-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="3f14a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f14a-108">EXAMPLES</span></span>

### <span data-ttu-id="3f14a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f14a-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3f14a-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="3f14a-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="3f14a-111">OS</span><span class="sxs-lookup"><span data-stu-id="3f14a-111">PARAMETERS</span></span>

### <span data-ttu-id="3f14a-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="3f14a-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="3f14a-113">Nomes distintos dos grupos do Active Directory que estarão disponíveis no Ambari e no Ranger</span><span class="sxs-lookup"><span data-stu-id="3f14a-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-114">-Config</span><span class="sxs-lookup"><span data-stu-id="3f14a-114">-Config</span></span>
<span data-ttu-id="3f14a-115">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3f14a-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3f14a-116">Esse objeto é criado pelo cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3f14a-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f14a-117">-DefaultProfile</span></span>
<span data-ttu-id="3f14a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3f14a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="3f14a-119">-Domain</span></span>
<span data-ttu-id="3f14a-120">Domínio do Active Directory para o cluster</span><span class="sxs-lookup"><span data-stu-id="3f14a-120">Active Directory domain for the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="3f14a-121">-DomainUserCredential</span></span>
<span data-ttu-id="3f14a-122">Uma credencial de conta de usuário do domínio com permissões suficientes para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="3f14a-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="3f14a-123">O nome de usuário deve estar em user@domain formato</span><span class="sxs-lookup"><span data-stu-id="3f14a-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="3f14a-124">-LdapsUrls</span></span>
<span data-ttu-id="3f14a-125">URLs de um ou vários servidores LDAPs para o Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f14a-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="3f14a-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="3f14a-127">Nome diferenciado da unidade organizacional no Active Directory onde as contas de usuário e de computador serão criadas</span><span class="sxs-lookup"><span data-stu-id="3f14a-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f14a-128">-Confirm</span></span>
<span data-ttu-id="3f14a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f14a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f14a-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f14a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f14a-131">CommonParameters</span></span>
<span data-ttu-id="3f14a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f14a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f14a-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f14a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f14a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f14a-134">INPUTS</span></span>

### <span data-ttu-id="3f14a-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3f14a-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="3f14a-136">Parâmetros: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f14a-136">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="3f14a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f14a-137">OUTPUTS</span></span>

### <span data-ttu-id="3f14a-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3f14a-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="3f14a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f14a-139">NOTES</span></span>

## <span data-ttu-id="3f14a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f14a-140">RELATED LINKS</span></span>
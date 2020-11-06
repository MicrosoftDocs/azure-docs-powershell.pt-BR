---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433386"
---
# <span data-ttu-id="79bc3-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79bc3-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="79bc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="79bc3-103">Cria um plano de recuperação de site na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="79bc3-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79bc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79bc3-104">SYNTAX</span></span>

### <span data-ttu-id="79bc3-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="79bc3-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79bc3-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="79bc3-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79bc3-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="79bc3-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79bc3-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="79bc3-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79bc3-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="79bc3-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79bc3-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="79bc3-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79bc3-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79bc3-111">DESCRIPTION</span></span>
<span data-ttu-id="79bc3-112">O cmdlet **New-AzureRmSiteRecoveryRecoveryPlan** cria um plano de recuperação no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="79bc3-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="79bc3-113">Um plano de recuperação reúne máquinas virtuais em um grupo para fins de failover e recuperação.</span><span class="sxs-lookup"><span data-stu-id="79bc3-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="79bc3-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79bc3-114">EXAMPLES</span></span>

### <span data-ttu-id="79bc3-115">Exemplo 1: adicionar um plano de recuperação a um cofre de recuperação de site</span><span class="sxs-lookup"><span data-stu-id="79bc3-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="79bc3-116">Esse comando adiciona o plano de recuperação chamado RecoveryPlan.xml ao cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="79bc3-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="79bc3-117">OS</span><span class="sxs-lookup"><span data-stu-id="79bc3-117">PARAMETERS</span></span>

### <span data-ttu-id="79bc3-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="79bc3-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bc3-119">-DefaultProfile</span></span>
<span data-ttu-id="79bc3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79bc3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="79bc3-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="79bc3-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="79bc3-123">-Path</span></span>
<span data-ttu-id="79bc3-124">Especifica o caminho do arquivo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="79bc3-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="79bc3-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="79bc3-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="79bc3-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="79bc3-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="79bc3-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="79bc3-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79bc3-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79bc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bc3-132">CommonParameters</span></span>
<span data-ttu-id="79bc3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bc3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79bc3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bc3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79bc3-135">INPUTS</span></span>

### <span data-ttu-id="79bc3-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="79bc3-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="79bc3-137">O parâmetro ' ProtectionEntityList ' aceita o valor do tipo ' ASRProtectionEntity [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="79bc3-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="79bc3-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="79bc3-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="79bc3-139">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem [] ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="79bc3-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="79bc3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79bc3-140">OUTPUTS</span></span>

## <span data-ttu-id="79bc3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79bc3-141">NOTES</span></span>

## <span data-ttu-id="79bc3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79bc3-142">RELATED LINKS</span></span>

[<span data-ttu-id="79bc3-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79bc3-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="79bc3-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79bc3-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="79bc3-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79bc3-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)



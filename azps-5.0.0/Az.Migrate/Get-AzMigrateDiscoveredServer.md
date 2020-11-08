---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126017"
---
# <span data-ttu-id="101e3-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="101e3-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="101e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="101e3-102">SYNOPSIS</span></span>
<span data-ttu-id="101e3-103">Obter todos os servidores descobertos em um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="101e3-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="101e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="101e3-104">SYNTAX</span></span>

### <span data-ttu-id="101e3-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="101e3-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="101e3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="101e3-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="101e3-107">Insite</span><span class="sxs-lookup"><span data-stu-id="101e3-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="101e3-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="101e3-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="101e3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="101e3-109">DESCRIPTION</span></span>
<span data-ttu-id="101e3-110">Obter Azure migre Server commandlet busca todos os servidores em um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="101e3-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="101e3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="101e3-111">EXAMPLES</span></span>

### <span data-ttu-id="101e3-112">Exemplo 1: lista</span><span class="sxs-lookup"><span data-stu-id="101e3-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="101e3-113">Obter todos os servidores em um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="101e3-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="101e3-114">Exemplo 2: obter</span><span class="sxs-lookup"><span data-stu-id="101e3-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="101e3-115">Obtenha um servidor em um projeto de migração por nome.</span><span class="sxs-lookup"><span data-stu-id="101e3-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="101e3-116">Nome é um único contratador exclusivo para um servidor.</span><span class="sxs-lookup"><span data-stu-id="101e3-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="101e3-117">Exemplo 3: lista em um aparelho</span><span class="sxs-lookup"><span data-stu-id="101e3-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="101e3-118">Liste todos os servidores de um dispositivo em um projeto.</span><span class="sxs-lookup"><span data-stu-id="101e3-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="101e3-119">Exemplo 4: obter em um aparelho</span><span class="sxs-lookup"><span data-stu-id="101e3-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="101e3-120">Obter um servidor para um aparelho em um projeto.</span><span class="sxs-lookup"><span data-stu-id="101e3-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="101e3-121">Nome é um único contratador exclusivo para um servidor.</span><span class="sxs-lookup"><span data-stu-id="101e3-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="101e3-122">Exemplo 5: listar e filtrar por nome para exibição</span><span class="sxs-lookup"><span data-stu-id="101e3-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="101e3-123">Liste os servidores em migrar as respostas de projeto e de filtro com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="101e3-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="101e3-124">Exemplo 6: lista em um aparelho e filtrar por nome para exibição</span><span class="sxs-lookup"><span data-stu-id="101e3-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="101e3-125">Servidores de lista para um dispositivo em migrar um projeto e respostas de filtro com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="101e3-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="101e3-126">OS</span><span class="sxs-lookup"><span data-stu-id="101e3-126">PARAMETERS</span></span>

### <span data-ttu-id="101e3-127">-Reaparelhoname</span><span class="sxs-lookup"><span data-stu-id="101e3-127">-ApplianceName</span></span>
<span data-ttu-id="101e3-128">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="101e3-128">Specifies the appliance name.</span></span>
<span data-ttu-id="101e3-129">Isso é mapeado internamente para um site.</span><span class="sxs-lookup"><span data-stu-id="101e3-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101e3-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="101e3-130">-DisplayName</span></span>
<span data-ttu-id="101e3-131">Especifica o nome de exibição do computador VMware.</span><span class="sxs-lookup"><span data-stu-id="101e3-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101e3-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="101e3-132">-Name</span></span>
<span data-ttu-id="101e3-133">Especifica o nome do computador VMware.</span><span class="sxs-lookup"><span data-stu-id="101e3-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="101e3-134">Este é um nome interno.</span><span class="sxs-lookup"><span data-stu-id="101e3-134">This is an internal Name.</span></span>
<span data-ttu-id="101e3-135">Para usuários, use o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="101e3-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101e3-136">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="101e3-136">-ProjectName</span></span>
<span data-ttu-id="101e3-137">Especifica o nome do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="101e3-137">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="101e3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="101e3-138">-ResourceGroupName</span></span>
<span data-ttu-id="101e3-139">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="101e3-139">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="101e3-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="101e3-140">-SubscriptionId</span></span>
<span data-ttu-id="101e3-141">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="101e3-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101e3-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="101e3-142">-Confirm</span></span>
<span data-ttu-id="101e3-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="101e3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="101e3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="101e3-144">-WhatIf</span></span>
<span data-ttu-id="101e3-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="101e3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="101e3-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="101e3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="101e3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101e3-147">CommonParameters</span></span>
<span data-ttu-id="101e3-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="101e3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101e3-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="101e3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101e3-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="101e3-150">INPUTS</span></span>

## <span data-ttu-id="101e3-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="101e3-151">OUTPUTS</span></span>

### <span data-ttu-id="101e3-152">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api202001. IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="101e3-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="101e3-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="101e3-153">NOTES</span></span>

<span data-ttu-id="101e3-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="101e3-154">ALIASES</span></span>

## <span data-ttu-id="101e3-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="101e3-155">RELATED LINKS</span></span>


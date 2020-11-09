---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280582"
---
# <span data-ttu-id="85d96-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="85d96-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="85d96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85d96-102">SYNOPSIS</span></span>
<span data-ttu-id="85d96-103">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="85d96-103">Get an application group.</span></span>

## <span data-ttu-id="85d96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85d96-104">SYNTAX</span></span>

### <span data-ttu-id="85d96-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="85d96-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="85d96-106">Obter</span><span class="sxs-lookup"><span data-stu-id="85d96-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85d96-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85d96-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="85d96-108">Programação</span><span class="sxs-lookup"><span data-stu-id="85d96-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="85d96-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85d96-109">DESCRIPTION</span></span>
<span data-ttu-id="85d96-110">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="85d96-110">Get an application group.</span></span>

## <span data-ttu-id="85d96-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85d96-111">EXAMPLES</span></span>

### <span data-ttu-id="85d96-112">Exemplo 1: obter um aplicativo de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="85d96-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="85d96-113">Este comando obtém um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85d96-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="85d96-114">Exemplo 2: lista ApplicationGroups da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="85d96-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="85d96-115">Esse comando lista um ApplicationGroups da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85d96-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="85d96-116">OS</span><span class="sxs-lookup"><span data-stu-id="85d96-116">PARAMETERS</span></span>

### <span data-ttu-id="85d96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d96-117">-DefaultProfile</span></span>
<span data-ttu-id="85d96-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85d96-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="85d96-119">-Filter</span></span>
<span data-ttu-id="85d96-120">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="85d96-120">OData filter expression.</span></span>
<span data-ttu-id="85d96-121">As propriedades válidas para filtragem são applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="85d96-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85d96-122">-InputObject</span></span>
<span data-ttu-id="85d96-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="85d96-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="85d96-124">-Name</span></span>
<span data-ttu-id="85d96-125">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="85d96-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d96-126">-ResourceGroupName</span></span>
<span data-ttu-id="85d96-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85d96-127">The name of the resource group.</span></span>
<span data-ttu-id="85d96-128">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85d96-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85d96-129">-SubscriptionId</span></span>
<span data-ttu-id="85d96-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="85d96-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85d96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d96-131">CommonParameters</span></span>
<span data-ttu-id="85d96-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d96-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d96-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d96-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85d96-134">INPUTS</span></span>

### <span data-ttu-id="85d96-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="85d96-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="85d96-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85d96-136">OUTPUTS</span></span>

### <span data-ttu-id="85d96-137">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="85d96-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="85d96-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85d96-138">NOTES</span></span>

<span data-ttu-id="85d96-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="85d96-139">ALIASES</span></span>

<span data-ttu-id="85d96-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="85d96-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85d96-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="85d96-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85d96-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85d96-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85d96-143">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="85d96-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85d96-144">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="85d96-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="85d96-145">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="85d96-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="85d96-146">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="85d96-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="85d96-147">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="85d96-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="85d96-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="85d96-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85d96-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85d96-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="85d96-150">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85d96-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="85d96-151">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="85d96-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="85d96-152">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="85d96-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="85d96-153">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="85d96-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="85d96-154">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="85d96-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="85d96-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85d96-155">RELATED LINKS</span></span>


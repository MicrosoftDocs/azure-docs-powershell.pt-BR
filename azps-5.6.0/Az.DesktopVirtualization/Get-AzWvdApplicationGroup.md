---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: e5cef84d4ae45e4ce55b1f377ab16edc2449c72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886642"
---
# <span data-ttu-id="2ac3a-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2ac3a-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="2ac3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac3a-103">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-103">Get an application group.</span></span>

## <span data-ttu-id="2ac3a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ac3a-104">SYNTAX</span></span>

### <span data-ttu-id="2ac3a-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ac3a-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac3a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2ac3a-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ac3a-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac3a-108">Listar</span><span class="sxs-lookup"><span data-stu-id="2ac3a-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2ac3a-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ac3a-109">DESCRIPTION</span></span>
<span data-ttu-id="2ac3a-110">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-110">Get an application group.</span></span>

## <span data-ttu-id="2ac3a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-111">EXAMPLES</span></span>

### <span data-ttu-id="2ac3a-112">Exemplo 1: Obter um Grupo de Aplicativos de Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="2ac3a-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="2ac3a-113">Este comando obtém um Windows Virtual Desktop ApplicationGroup em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="2ac3a-114">Exemplo 2: Listar Grupos de Aplicativos de Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="2ac3a-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="2ac3a-115">Este comando lista um Windows Virtual Desktop ApplicationGroups em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="2ac3a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-116">PARAMETERS</span></span>

### <span data-ttu-id="2ac3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac3a-117">-DefaultProfile</span></span>
<span data-ttu-id="2ac3a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac3a-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="2ac3a-119">-Filter</span></span>
<span data-ttu-id="2ac3a-120">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-120">OData filter expression.</span></span>
<span data-ttu-id="2ac3a-121">As propriedades válidas para filtragem são applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="2ac3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac3a-122">-InputObject</span></span>
<span data-ttu-id="2ac3a-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ac3a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2ac3a-124">-Name</span></span>
<span data-ttu-id="2ac3a-125">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2ac3a-125">The name of the application group</span></span>

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

### <span data-ttu-id="2ac3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ac3a-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-127">The name of the resource group.</span></span>
<span data-ttu-id="2ac3a-128">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ac3a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ac3a-129">-SubscriptionId</span></span>
<span data-ttu-id="2ac3a-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ac3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac3a-131">CommonParameters</span></span>
<span data-ttu-id="2ac3a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac3a-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ac3a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac3a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-134">INPUTS</span></span>

### <span data-ttu-id="2ac3a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2ac3a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2ac3a-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-136">OUTPUTS</span></span>

### <span data-ttu-id="2ac3a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2ac3a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="2ac3a-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ac3a-138">NOTES</span></span>

<span data-ttu-id="2ac3a-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2ac3a-139">ALIASES</span></span>

<span data-ttu-id="2ac3a-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2ac3a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ac3a-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ac3a-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ac3a-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2ac3a-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ac3a-144">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2ac3a-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2ac3a-145">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2ac3a-146">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2ac3a-147">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2ac3a-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2ac3a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ac3a-149">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2ac3a-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ac3a-151">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ac3a-152">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2ac3a-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2ac3a-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ac3a-154">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="2ac3a-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2ac3a-155">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2ac3a-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2ac3a-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ac3a-156">RELATED LINKS</span></span>


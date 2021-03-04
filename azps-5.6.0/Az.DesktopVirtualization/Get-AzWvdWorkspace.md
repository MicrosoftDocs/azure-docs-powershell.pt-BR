---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 331026116b59e71d57b4ea440b53a1445ea7642b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888955"
---
# <span data-ttu-id="cca06-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="cca06-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="cca06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca06-102">SYNOPSIS</span></span>
<span data-ttu-id="cca06-103">Obter um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca06-103">Get a workspace.</span></span>

## <span data-ttu-id="cca06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cca06-104">SYNTAX</span></span>

### <span data-ttu-id="cca06-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cca06-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cca06-106">Obter</span><span class="sxs-lookup"><span data-stu-id="cca06-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cca06-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cca06-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cca06-108">Listar</span><span class="sxs-lookup"><span data-stu-id="cca06-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cca06-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cca06-109">DESCRIPTION</span></span>
<span data-ttu-id="cca06-110">Obter um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cca06-110">Get a workspace.</span></span>

## <span data-ttu-id="cca06-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cca06-111">EXAMPLES</span></span>

### <span data-ttu-id="cca06-112">Exemplo 1: Obter um Espaço de Trabalho da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="cca06-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="cca06-113">Este comando obtém um Espaço de Trabalho da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="cca06-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="cca06-114">Exemplo 2: Listar espaços de trabalho da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="cca06-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="cca06-115">Este comando lista um Espaço de Trabalho da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="cca06-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="cca06-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cca06-116">PARAMETERS</span></span>

### <span data-ttu-id="cca06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca06-117">-DefaultProfile</span></span>
<span data-ttu-id="cca06-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cca06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca06-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cca06-119">-InputObject</span></span>
<span data-ttu-id="cca06-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cca06-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cca06-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cca06-121">-Name</span></span>
<span data-ttu-id="cca06-122">O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="cca06-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca06-123">-ResourceGroupName</span></span>
<span data-ttu-id="cca06-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cca06-124">The name of the resource group.</span></span>
<span data-ttu-id="cca06-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cca06-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cca06-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cca06-126">-SubscriptionId</span></span>
<span data-ttu-id="cca06-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cca06-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cca06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca06-128">CommonParameters</span></span>
<span data-ttu-id="cca06-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca06-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cca06-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca06-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cca06-131">INPUTS</span></span>

### <span data-ttu-id="cca06-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cca06-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cca06-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cca06-133">OUTPUTS</span></span>

### <span data-ttu-id="cca06-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="cca06-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="cca06-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="cca06-135">NOTES</span></span>

<span data-ttu-id="cca06-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cca06-136">ALIASES</span></span>

<span data-ttu-id="cca06-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cca06-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cca06-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cca06-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cca06-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cca06-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cca06-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="cca06-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cca06-141">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="cca06-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cca06-142">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cca06-143">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cca06-144">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cca06-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cca06-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cca06-146">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cca06-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cca06-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cca06-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cca06-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="cca06-149">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cca06-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cca06-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cca06-151">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="cca06-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cca06-152">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="cca06-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cca06-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cca06-153">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: b7aa21b07726140f8f6514fe8d7b6dc9a4b191dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886643"
---
# <span data-ttu-id="6beac-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="6beac-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="6beac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beac-102">SYNOPSIS</span></span>
<span data-ttu-id="6beac-103">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6beac-103">Get an application.</span></span>

## <span data-ttu-id="6beac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6beac-104">SYNTAX</span></span>

### <span data-ttu-id="6beac-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6beac-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6beac-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6beac-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6beac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6beac-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6beac-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6beac-108">DESCRIPTION</span></span>
<span data-ttu-id="6beac-109">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6beac-109">Get an application.</span></span>

## <span data-ttu-id="6beac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6beac-110">EXAMPLES</span></span>

### <span data-ttu-id="6beac-111">Exemplo 1: obter um aplicativo de área de trabalho virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="6beac-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="6beac-112">Este comando obtém um Aplicativo de Área de Trabalho Virtual do Windows em um grupo de aplicações.</span><span class="sxs-lookup"><span data-stu-id="6beac-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="6beac-113">Exemplo 2: Listar aplicativos de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="6beac-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="6beac-114">Este comando lista aplicativos de área de trabalho virtual do Windows em um grupo de aplicação.</span><span class="sxs-lookup"><span data-stu-id="6beac-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="6beac-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6beac-115">PARAMETERS</span></span>

### <span data-ttu-id="6beac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beac-116">-DefaultProfile</span></span>
<span data-ttu-id="6beac-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6beac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beac-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="6beac-118">-GroupName</span></span>
<span data-ttu-id="6beac-119">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6beac-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6beac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6beac-120">-InputObject</span></span>
<span data-ttu-id="6beac-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6beac-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6beac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6beac-122">-Name</span></span>
<span data-ttu-id="6beac-123">O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6beac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beac-124">-ResourceGroupName</span></span>
<span data-ttu-id="6beac-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6beac-125">The name of the resource group.</span></span>
<span data-ttu-id="6beac-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6beac-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6beac-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6beac-127">-SubscriptionId</span></span>
<span data-ttu-id="6beac-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6beac-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6beac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beac-129">CommonParameters</span></span>
<span data-ttu-id="6beac-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6beac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beac-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6beac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beac-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6beac-132">INPUTS</span></span>

### <span data-ttu-id="6beac-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6beac-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6beac-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6beac-134">OUTPUTS</span></span>

### <span data-ttu-id="6beac-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="6beac-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="6beac-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="6beac-136">NOTES</span></span>

<span data-ttu-id="6beac-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6beac-137">ALIASES</span></span>

<span data-ttu-id="6beac-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6beac-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6beac-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6beac-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6beac-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6beac-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6beac-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6beac-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6beac-142">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6beac-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6beac-143">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6beac-144">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6beac-145">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6beac-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6beac-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6beac-147">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6beac-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6beac-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6beac-149">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6beac-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="6beac-150">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6beac-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6beac-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6beac-152">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="6beac-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6beac-153">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="6beac-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6beac-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6beac-154">RELATED LINKS</span></span>


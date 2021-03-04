---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 2c276ab6b791d041000adf872bf2bfb807032ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888959"
---
# <span data-ttu-id="eb683-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="eb683-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="eb683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb683-102">SYNOPSIS</span></span>
<span data-ttu-id="eb683-103">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eb683-103">Get a desktop.</span></span>

## <span data-ttu-id="eb683-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb683-104">SYNTAX</span></span>

### <span data-ttu-id="eb683-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eb683-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb683-106">Obter</span><span class="sxs-lookup"><span data-stu-id="eb683-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb683-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb683-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb683-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb683-108">DESCRIPTION</span></span>
<span data-ttu-id="eb683-109">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eb683-109">Get a desktop.</span></span>

## <span data-ttu-id="eb683-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb683-110">EXAMPLES</span></span>

### <span data-ttu-id="eb683-111">Exemplo 1: Obter um nome de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="eb683-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="eb683-112">Este comando obtém uma Área de Trabalho Virtual do Windows em um grupo de aplicações.</span><span class="sxs-lookup"><span data-stu-id="eb683-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="eb683-113">Exemplo 2: Listar áreas de trabalho virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="eb683-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="eb683-114">Este comando listaWindows Virtual Desktops in an applicaton Group.</span><span class="sxs-lookup"><span data-stu-id="eb683-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="eb683-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb683-115">PARAMETERS</span></span>

### <span data-ttu-id="eb683-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="eb683-116">-ApplicationGroupName</span></span>
<span data-ttu-id="eb683-117">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="eb683-117">The name of the application group</span></span>

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

### <span data-ttu-id="eb683-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb683-118">-DefaultProfile</span></span>
<span data-ttu-id="eb683-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb683-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb683-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb683-120">-InputObject</span></span>
<span data-ttu-id="eb683-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="eb683-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb683-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eb683-122">-Name</span></span>
<span data-ttu-id="eb683-123">O nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb683-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb683-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb683-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb683-125">The name of the resource group.</span></span>
<span data-ttu-id="eb683-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eb683-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="eb683-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb683-127">-SubscriptionId</span></span>
<span data-ttu-id="eb683-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="eb683-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eb683-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb683-129">CommonParameters</span></span>
<span data-ttu-id="eb683-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb683-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb683-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb683-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb683-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb683-132">INPUTS</span></span>

### <span data-ttu-id="eb683-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="eb683-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="eb683-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb683-134">OUTPUTS</span></span>

### <span data-ttu-id="eb683-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="eb683-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="eb683-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="eb683-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="eb683-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb683-137">NOTES</span></span>

<span data-ttu-id="eb683-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="eb683-138">ALIASES</span></span>

<span data-ttu-id="eb683-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="eb683-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb683-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="eb683-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb683-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb683-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb683-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="eb683-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb683-143">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="eb683-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="eb683-144">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="eb683-145">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="eb683-146">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="eb683-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="eb683-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb683-148">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="eb683-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb683-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eb683-150">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eb683-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="eb683-151">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="eb683-152">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="eb683-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eb683-153">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="eb683-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="eb683-154">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="eb683-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="eb683-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb683-155">RELATED LINKS</span></span>


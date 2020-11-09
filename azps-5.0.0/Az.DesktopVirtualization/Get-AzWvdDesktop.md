---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280577"
---
# <span data-ttu-id="fba9e-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="fba9e-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="fba9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fba9e-102">SYNOPSIS</span></span>
<span data-ttu-id="fba9e-103">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fba9e-103">Get a desktop.</span></span>

## <span data-ttu-id="fba9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fba9e-104">SYNTAX</span></span>

### <span data-ttu-id="fba9e-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="fba9e-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fba9e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fba9e-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fba9e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fba9e-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fba9e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fba9e-108">DESCRIPTION</span></span>
<span data-ttu-id="fba9e-109">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fba9e-109">Get a desktop.</span></span>

## <span data-ttu-id="fba9e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fba9e-110">EXAMPLES</span></span>

### <span data-ttu-id="fba9e-111">Exemplo 1: obter uma área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="fba9e-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="fba9e-112">Esse comando obtém uma área de trabalho da área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="fba9e-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="fba9e-113">Exemplo 2: listar áreas de trabalho da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="fba9e-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="fba9e-114">Este comando listsWindows áreas de trabalho virtual de área de trabalho em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="fba9e-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="fba9e-115">OS</span><span class="sxs-lookup"><span data-stu-id="fba9e-115">PARAMETERS</span></span>

### <span data-ttu-id="fba9e-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="fba9e-116">-ApplicationGroupName</span></span>
<span data-ttu-id="fba9e-117">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="fba9e-117">The name of the application group</span></span>

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

### <span data-ttu-id="fba9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba9e-118">-DefaultProfile</span></span>
<span data-ttu-id="fba9e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fba9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fba9e-120">-InputObject</span></span>
<span data-ttu-id="fba9e-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fba9e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fba9e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fba9e-122">-Name</span></span>
<span data-ttu-id="fba9e-123">O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="fba9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="fba9e-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fba9e-125">The name of the resource group.</span></span>
<span data-ttu-id="fba9e-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fba9e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fba9e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fba9e-127">-SubscriptionId</span></span>
<span data-ttu-id="fba9e-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fba9e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fba9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba9e-129">CommonParameters</span></span>
<span data-ttu-id="fba9e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba9e-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fba9e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba9e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fba9e-132">INPUTS</span></span>

### <span data-ttu-id="fba9e-133">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="fba9e-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fba9e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fba9e-134">OUTPUTS</span></span>

### <span data-ttu-id="fba9e-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="fba9e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="fba9e-136">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="fba9e-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="fba9e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fba9e-137">NOTES</span></span>

<span data-ttu-id="fba9e-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fba9e-138">ALIASES</span></span>

<span data-ttu-id="fba9e-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fba9e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fba9e-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fba9e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fba9e-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fba9e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fba9e-142">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fba9e-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fba9e-143">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="fba9e-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fba9e-144">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fba9e-145">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fba9e-146">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fba9e-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fba9e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fba9e-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fba9e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fba9e-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fba9e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="fba9e-150">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fba9e-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fba9e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fba9e-152">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="fba9e-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fba9e-153">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fba9e-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fba9e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fba9e-154">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112273"
---
# <span data-ttu-id="3d2be-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="3d2be-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="3d2be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d2be-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2be-103">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d2be-103">Get an application.</span></span>

## <span data-ttu-id="3d2be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d2be-104">SYNTAX</span></span>

### <span data-ttu-id="3d2be-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d2be-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d2be-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3d2be-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d2be-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d2be-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d2be-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d2be-108">DESCRIPTION</span></span>
<span data-ttu-id="3d2be-109">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d2be-109">Get an application.</span></span>

## <span data-ttu-id="3d2be-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d2be-110">EXAMPLES</span></span>

### <span data-ttu-id="3d2be-111">Exemplo 1: obter um aplicativo de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="3d2be-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="3d2be-112">Esse comando obtém um aplicativo de área de trabalho virtual do Windows em um grupo applicaton.</span><span class="sxs-lookup"><span data-stu-id="3d2be-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="3d2be-113">Exemplo 2: listar aplicativos da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="3d2be-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="3d2be-114">Esse comando lista os aplicativos da área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="3d2be-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="3d2be-115">OS</span><span class="sxs-lookup"><span data-stu-id="3d2be-115">PARAMETERS</span></span>

### <span data-ttu-id="3d2be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2be-116">-DefaultProfile</span></span>
<span data-ttu-id="3d2be-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d2be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d2be-118">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="3d2be-118">-GroupName</span></span>
<span data-ttu-id="3d2be-119">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3d2be-119">The name of the application group</span></span>

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

### <span data-ttu-id="3d2be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d2be-120">-InputObject</span></span>
<span data-ttu-id="3d2be-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3d2be-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d2be-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d2be-122">-Name</span></span>
<span data-ttu-id="3d2be-123">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="3d2be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2be-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d2be-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d2be-125">The name of the resource group.</span></span>
<span data-ttu-id="3d2be-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3d2be-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3d2be-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d2be-127">-SubscriptionId</span></span>
<span data-ttu-id="3d2be-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3d2be-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3d2be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2be-129">CommonParameters</span></span>
<span data-ttu-id="3d2be-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2be-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d2be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2be-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d2be-132">INPUTS</span></span>

### <span data-ttu-id="3d2be-133">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3d2be-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3d2be-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d2be-134">OUTPUTS</span></span>

### <span data-ttu-id="3d2be-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="3d2be-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="3d2be-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d2be-136">NOTES</span></span>

<span data-ttu-id="3d2be-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3d2be-137">ALIASES</span></span>

<span data-ttu-id="3d2be-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3d2be-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d2be-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3d2be-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d2be-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d2be-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d2be-141">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3d2be-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d2be-142">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3d2be-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3d2be-143">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3d2be-144">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3d2be-145">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3d2be-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3d2be-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d2be-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d2be-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3d2be-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3d2be-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="3d2be-149">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3d2be-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3d2be-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3d2be-151">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="3d2be-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3d2be-152">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3d2be-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3d2be-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d2be-153">RELATED LINKS</span></span>


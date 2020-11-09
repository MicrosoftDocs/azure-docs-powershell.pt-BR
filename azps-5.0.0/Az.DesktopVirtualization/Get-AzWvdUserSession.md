---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280569"
---
# <span data-ttu-id="89097-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="89097-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="89097-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89097-102">SYNOPSIS</span></span>
<span data-ttu-id="89097-103">Obter um usersession.</span><span class="sxs-lookup"><span data-stu-id="89097-103">Get a userSession.</span></span>

## <span data-ttu-id="89097-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89097-104">SYNTAX</span></span>

### <span data-ttu-id="89097-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="89097-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89097-106">Obter</span><span class="sxs-lookup"><span data-stu-id="89097-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89097-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89097-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="89097-108">List1</span><span class="sxs-lookup"><span data-stu-id="89097-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89097-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89097-109">DESCRIPTION</span></span>
<span data-ttu-id="89097-110">Obter um usersession.</span><span class="sxs-lookup"><span data-stu-id="89097-110">Get a userSession.</span></span>

## <span data-ttu-id="89097-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89097-111">EXAMPLES</span></span>

### <span data-ttu-id="89097-112">Exemplo 1: obter um usersession da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="89097-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="89097-113">Este comando obtém uma sessão do userdesktop virtual do Windows em um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="89097-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="89097-114">Exemplo 2: listar os usersessions da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="89097-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="89097-115">Esse comando lista um usersessions de área de trabalho virtual do Windows em um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="89097-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="89097-116">Exemplo 3: listar as sessões do userdesktop virtual do Windows no pool do host</span><span class="sxs-lookup"><span data-stu-id="89097-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="89097-117">Esse comando lista um usersessions de área de trabalho virtual do Windows em um host de sessão em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="89097-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="89097-118">OS</span><span class="sxs-lookup"><span data-stu-id="89097-118">PARAMETERS</span></span>

### <span data-ttu-id="89097-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89097-119">-DefaultProfile</span></span>
<span data-ttu-id="89097-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89097-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89097-121">-Filtro</span><span class="sxs-lookup"><span data-stu-id="89097-121">-Filter</span></span>
<span data-ttu-id="89097-122">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="89097-122">OData filter expression.</span></span>
<span data-ttu-id="89097-123">As propriedades válidas para filtragem são userPrincipalName e SessionState.</span><span class="sxs-lookup"><span data-stu-id="89097-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89097-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="89097-124">-HostPoolName</span></span>
<span data-ttu-id="89097-125">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="89097-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89097-126">-ID</span><span class="sxs-lookup"><span data-stu-id="89097-126">-Id</span></span>
<span data-ttu-id="89097-127">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="89097-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89097-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89097-128">-InputObject</span></span>
<span data-ttu-id="89097-129">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="89097-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89097-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89097-130">-ResourceGroupName</span></span>
<span data-ttu-id="89097-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89097-131">The name of the resource group.</span></span>
<span data-ttu-id="89097-132">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="89097-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89097-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="89097-133">-SessionHostName</span></span>
<span data-ttu-id="89097-134">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="89097-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89097-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89097-135">-SubscriptionId</span></span>
<span data-ttu-id="89097-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="89097-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89097-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89097-137">CommonParameters</span></span>
<span data-ttu-id="89097-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89097-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89097-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89097-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89097-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89097-140">INPUTS</span></span>

### <span data-ttu-id="89097-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="89097-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="89097-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89097-142">OUTPUTS</span></span>

### <span data-ttu-id="89097-143">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="89097-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="89097-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89097-144">NOTES</span></span>

<span data-ttu-id="89097-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="89097-145">ALIASES</span></span>

<span data-ttu-id="89097-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="89097-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89097-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="89097-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89097-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89097-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89097-149">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="89097-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89097-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="89097-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="89097-151">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="89097-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="89097-152">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="89097-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="89097-153">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="89097-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="89097-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="89097-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89097-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89097-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89097-156">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="89097-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="89097-157">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="89097-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="89097-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="89097-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="89097-159">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="89097-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="89097-160">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="89097-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="89097-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89097-161">RELATED LINKS</span></span>


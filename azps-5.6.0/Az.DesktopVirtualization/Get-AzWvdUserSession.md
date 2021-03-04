---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: a19d1e39fb9ef2e982b569b8c0351d8d1bde1fb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887158"
---
# <span data-ttu-id="dc349-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="dc349-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="dc349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc349-102">SYNOPSIS</span></span>
<span data-ttu-id="dc349-103">Obter uma userSession.</span><span class="sxs-lookup"><span data-stu-id="dc349-103">Get a userSession.</span></span>

## <span data-ttu-id="dc349-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc349-104">SYNTAX</span></span>

### <span data-ttu-id="dc349-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc349-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc349-106">Obter</span><span class="sxs-lookup"><span data-stu-id="dc349-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc349-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc349-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc349-108">List1</span><span class="sxs-lookup"><span data-stu-id="dc349-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc349-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc349-109">DESCRIPTION</span></span>
<span data-ttu-id="dc349-110">Obter uma userSession.</span><span class="sxs-lookup"><span data-stu-id="dc349-110">Get a userSession.</span></span>

## <span data-ttu-id="dc349-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc349-111">EXAMPLES</span></span>

### <span data-ttu-id="dc349-112">Exemplo 1: Obter um UserSession da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="dc349-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="dc349-113">Este comando obtém uma UserSession da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="dc349-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="dc349-114">Exemplo 2: Listar UserSessions da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="dc349-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="dc349-115">Este comando lista um UserSessions da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="dc349-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="dc349-116">Exemplo 3: Listar Usuários da Área de Trabalho Virtual do WindowsSessions no pool de host</span><span class="sxs-lookup"><span data-stu-id="dc349-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="dc349-117">Este comando lista um UserSessions da Área de Trabalho Virtual do Windows em um Host de Sessão em um pool de host.</span><span class="sxs-lookup"><span data-stu-id="dc349-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="dc349-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc349-118">PARAMETERS</span></span>

### <span data-ttu-id="dc349-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc349-119">-DefaultProfile</span></span>
<span data-ttu-id="dc349-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc349-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc349-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="dc349-121">-Filter</span></span>
<span data-ttu-id="dc349-122">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="dc349-122">OData filter expression.</span></span>
<span data-ttu-id="dc349-123">As propriedades válidas para filtragem são userprincipalname e sessionstate.</span><span class="sxs-lookup"><span data-stu-id="dc349-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="dc349-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="dc349-124">-HostPoolName</span></span>
<span data-ttu-id="dc349-125">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="dc349-126">-Id</span><span class="sxs-lookup"><span data-stu-id="dc349-126">-Id</span></span>
<span data-ttu-id="dc349-127">O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="dc349-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc349-128">-InputObject</span></span>
<span data-ttu-id="dc349-129">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dc349-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc349-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc349-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc349-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc349-131">The name of the resource group.</span></span>
<span data-ttu-id="dc349-132">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc349-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dc349-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="dc349-133">-SessionHostName</span></span>
<span data-ttu-id="dc349-134">O nome do host de sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="dc349-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc349-135">-SubscriptionId</span></span>
<span data-ttu-id="dc349-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dc349-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dc349-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc349-137">CommonParameters</span></span>
<span data-ttu-id="dc349-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc349-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc349-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc349-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc349-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc349-140">INPUTS</span></span>

### <span data-ttu-id="dc349-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dc349-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dc349-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc349-142">OUTPUTS</span></span>

### <span data-ttu-id="dc349-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="dc349-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="dc349-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc349-144">NOTES</span></span>

<span data-ttu-id="dc349-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dc349-145">ALIASES</span></span>

<span data-ttu-id="dc349-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="dc349-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc349-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dc349-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc349-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc349-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc349-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="dc349-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc349-150">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dc349-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dc349-151">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dc349-152">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dc349-153">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dc349-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="dc349-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc349-155">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dc349-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc349-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dc349-157">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc349-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="dc349-158">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dc349-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dc349-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dc349-160">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="dc349-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dc349-161">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="dc349-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dc349-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc349-162">RELATED LINKS</span></span>


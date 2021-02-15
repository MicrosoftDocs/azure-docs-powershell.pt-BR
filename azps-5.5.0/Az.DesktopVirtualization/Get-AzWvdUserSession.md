---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111909"
---
# <span data-ttu-id="a33d5-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="a33d5-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="a33d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a33d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a33d5-103">Obter uma usuária.</span><span class="sxs-lookup"><span data-stu-id="a33d5-103">Get a userSession.</span></span>

## <span data-ttu-id="a33d5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a33d5-104">SYNTAX</span></span>

### <span data-ttu-id="a33d5-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a33d5-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a33d5-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a33d5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a33d5-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33d5-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="a33d5-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a33d5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a33d5-109">DESCRIPTION</span></span>
<span data-ttu-id="a33d5-110">Obter uma usuária.</span><span class="sxs-lookup"><span data-stu-id="a33d5-110">Get a userSession.</span></span>

## <span data-ttu-id="a33d5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a33d5-111">EXAMPLES</span></span>

### <span data-ttu-id="a33d5-112">Exemplo 1: Obter uma UserSession da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="a33d5-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a33d5-113">Esse comando obtém uma UserSession da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="a33d5-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="a33d5-114">Exemplo 2: Listar UserSessions da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="a33d5-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a33d5-115">Este comando lista as UserSessionsão da Área de Trabalho Virtual do Windows em um Host de Sessão.</span><span class="sxs-lookup"><span data-stu-id="a33d5-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="a33d5-116">Exemplo 3: Listar UserSessions da Área de Trabalho Virtual do Windows no pool de host</span><span class="sxs-lookup"><span data-stu-id="a33d5-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="a33d5-117">Esse comando lista as UserSessionsão da Área de Trabalho Virtual do Windows em um Host de Sessão em um pool de host.</span><span class="sxs-lookup"><span data-stu-id="a33d5-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="a33d5-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a33d5-118">PARAMETERS</span></span>

### <span data-ttu-id="a33d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33d5-119">-DefaultProfile</span></span>
<span data-ttu-id="a33d5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a33d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a33d5-121">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a33d5-121">-Filter</span></span>
<span data-ttu-id="a33d5-122">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a33d5-122">OData filter expression.</span></span>
<span data-ttu-id="a33d5-123">As propriedades válidas para filtragem são userprincipalname e sessionstate.</span><span class="sxs-lookup"><span data-stu-id="a33d5-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="a33d5-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a33d5-124">-HostPoolName</span></span>
<span data-ttu-id="a33d5-125">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a33d5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a33d5-126">-Id</span></span>
<span data-ttu-id="a33d5-127">O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="a33d5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a33d5-128">-InputObject</span></span>
<span data-ttu-id="a33d5-129">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a33d5-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a33d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="a33d5-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a33d5-131">The name of the resource group.</span></span>
<span data-ttu-id="a33d5-132">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a33d5-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a33d5-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="a33d5-133">-SessionHostName</span></span>
<span data-ttu-id="a33d5-134">O nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="a33d5-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a33d5-135">-SubscriptionId</span></span>
<span data-ttu-id="a33d5-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a33d5-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a33d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33d5-137">CommonParameters</span></span>
<span data-ttu-id="a33d5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a33d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33d5-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a33d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33d5-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="a33d5-140">INPUTS</span></span>

### <span data-ttu-id="a33d5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a33d5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a33d5-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="a33d5-142">OUTPUTS</span></span>

### <span data-ttu-id="a33d5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="a33d5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="a33d5-144">Notas</span><span class="sxs-lookup"><span data-stu-id="a33d5-144">NOTES</span></span>

<span data-ttu-id="a33d5-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="a33d5-145">ALIASES</span></span>

<span data-ttu-id="a33d5-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a33d5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a33d5-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a33d5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a33d5-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a33d5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a33d5-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a33d5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a33d5-150">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a33d5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a33d5-151">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a33d5-152">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a33d5-153">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a33d5-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a33d5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a33d5-155">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a33d5-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a33d5-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a33d5-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a33d5-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a33d5-158">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a33d5-159">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a33d5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a33d5-160">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a33d5-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a33d5-161">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a33d5-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a33d5-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a33d5-162">RELATED LINKS</span></span>


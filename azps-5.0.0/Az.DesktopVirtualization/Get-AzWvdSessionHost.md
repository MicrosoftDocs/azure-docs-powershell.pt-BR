---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280568"
---
# <span data-ttu-id="e49a1-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="e49a1-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="e49a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e49a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e49a1-103">Obter um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="e49a1-103">Get a session host.</span></span>

## <span data-ttu-id="e49a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e49a1-104">SYNTAX</span></span>

### <span data-ttu-id="e49a1-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e49a1-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e49a1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e49a1-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e49a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e49a1-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e49a1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e49a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e49a1-109">Obter um host de sessão.</span><span class="sxs-lookup"><span data-stu-id="e49a1-109">Get a session host.</span></span>

## <span data-ttu-id="e49a1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e49a1-110">EXAMPLES</span></span>

### <span data-ttu-id="e49a1-111">Exemplo 1: obter um SessionHost de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="e49a1-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="e49a1-112">Este comando obtém um SessionHost da área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="e49a1-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="e49a1-113">Exemplo 2: lista SessionHosts da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="e49a1-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="e49a1-114">Esse comando lista um SessionHosts de área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="e49a1-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="e49a1-115">OS</span><span class="sxs-lookup"><span data-stu-id="e49a1-115">PARAMETERS</span></span>

### <span data-ttu-id="e49a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49a1-116">-DefaultProfile</span></span>
<span data-ttu-id="e49a1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e49a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49a1-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e49a1-118">-HostPoolName</span></span>
<span data-ttu-id="e49a1-119">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e49a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e49a1-120">-InputObject</span></span>
<span data-ttu-id="e49a1-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e49a1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e49a1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e49a1-122">-Name</span></span>
<span data-ttu-id="e49a1-123">O nome do host de sessão no pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e49a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e49a1-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e49a1-125">The name of the resource group.</span></span>
<span data-ttu-id="e49a1-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e49a1-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e49a1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e49a1-127">-SubscriptionId</span></span>
<span data-ttu-id="e49a1-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e49a1-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e49a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49a1-129">CommonParameters</span></span>
<span data-ttu-id="e49a1-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49a1-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e49a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49a1-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e49a1-132">INPUTS</span></span>

### <span data-ttu-id="e49a1-133">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e49a1-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e49a1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e49a1-134">OUTPUTS</span></span>

### <span data-ttu-id="e49a1-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="e49a1-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="e49a1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e49a1-136">NOTES</span></span>

<span data-ttu-id="e49a1-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e49a1-137">ALIASES</span></span>

<span data-ttu-id="e49a1-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e49a1-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e49a1-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e49a1-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e49a1-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e49a1-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e49a1-141">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e49a1-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e49a1-142">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="e49a1-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e49a1-143">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e49a1-144">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e49a1-145">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e49a1-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e49a1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e49a1-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e49a1-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e49a1-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e49a1-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="e49a1-149">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e49a1-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e49a1-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e49a1-151">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="e49a1-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e49a1-152">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e49a1-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e49a1-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e49a1-153">RELATED LINKS</span></span>


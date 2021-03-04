---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 1ba4b3141b2254de9e1988fbd2b76f03a06ceb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888958"
---
# <span data-ttu-id="19030-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="19030-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="19030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19030-102">SYNOPSIS</span></span>
<span data-ttu-id="19030-103">Obter um pool de host.</span><span class="sxs-lookup"><span data-stu-id="19030-103">Get a host pool.</span></span>

## <span data-ttu-id="19030-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19030-104">SYNTAX</span></span>

### <span data-ttu-id="19030-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="19030-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19030-106">Obter</span><span class="sxs-lookup"><span data-stu-id="19030-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19030-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19030-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="19030-108">Listar</span><span class="sxs-lookup"><span data-stu-id="19030-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="19030-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19030-109">DESCRIPTION</span></span>
<span data-ttu-id="19030-110">Obter um pool de host.</span><span class="sxs-lookup"><span data-stu-id="19030-110">Get a host pool.</span></span>

## <span data-ttu-id="19030-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19030-111">EXAMPLES</span></span>

### <span data-ttu-id="19030-112">Exemplo 1: Obter um HostPool da Área de Trabalho Virtual do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="19030-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="19030-113">Este comando obtém um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="19030-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="19030-114">Exemplo 2: Listar HostPools da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="19030-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="19030-115">Este comando lista um HostPools da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="19030-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="19030-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19030-116">PARAMETERS</span></span>

### <span data-ttu-id="19030-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19030-117">-DefaultProfile</span></span>
<span data-ttu-id="19030-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19030-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19030-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19030-119">-InputObject</span></span>
<span data-ttu-id="19030-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="19030-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19030-121">-Name</span><span class="sxs-lookup"><span data-stu-id="19030-121">-Name</span></span>
<span data-ttu-id="19030-122">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="19030-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19030-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19030-123">-ResourceGroupName</span></span>
<span data-ttu-id="19030-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19030-124">The name of the resource group.</span></span>
<span data-ttu-id="19030-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19030-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="19030-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19030-126">-SubscriptionId</span></span>
<span data-ttu-id="19030-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="19030-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="19030-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19030-128">CommonParameters</span></span>
<span data-ttu-id="19030-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19030-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19030-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19030-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19030-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19030-131">INPUTS</span></span>

### <span data-ttu-id="19030-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="19030-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="19030-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19030-133">OUTPUTS</span></span>

### <span data-ttu-id="19030-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="19030-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="19030-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="19030-135">NOTES</span></span>

<span data-ttu-id="19030-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="19030-136">ALIASES</span></span>

<span data-ttu-id="19030-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="19030-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19030-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="19030-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19030-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19030-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19030-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="19030-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19030-141">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="19030-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="19030-142">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="19030-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="19030-143">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="19030-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="19030-144">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="19030-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="19030-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="19030-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19030-146">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="19030-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="19030-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19030-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="19030-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19030-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="19030-149">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="19030-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="19030-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="19030-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="19030-151">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="19030-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="19030-152">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="19030-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="19030-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19030-153">RELATED LINKS</span></span>


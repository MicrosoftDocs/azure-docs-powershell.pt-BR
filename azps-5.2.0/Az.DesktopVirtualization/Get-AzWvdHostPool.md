---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 815f7280564d01077de99c4ec9b4003d4996d019
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257866"
---
# <span data-ttu-id="990d8-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="990d8-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="990d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="990d8-102">SYNOPSIS</span></span>
<span data-ttu-id="990d8-103">Obter um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="990d8-103">Get a host pool.</span></span>

## <span data-ttu-id="990d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="990d8-104">SYNTAX</span></span>

### <span data-ttu-id="990d8-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="990d8-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="990d8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="990d8-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="990d8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="990d8-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="990d8-108">Programação</span><span class="sxs-lookup"><span data-stu-id="990d8-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="990d8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="990d8-109">DESCRIPTION</span></span>
<span data-ttu-id="990d8-110">Obter um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="990d8-110">Get a host pool.</span></span>

## <span data-ttu-id="990d8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="990d8-111">EXAMPLES</span></span>

### <span data-ttu-id="990d8-112">Exemplo 1: obter um HostPool de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="990d8-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="990d8-113">Este comando obtém um HostPool da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="990d8-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="990d8-114">Exemplo 2: lista HostPools da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="990d8-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="990d8-115">Esse comando lista um HostPools da área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="990d8-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="990d8-116">OS</span><span class="sxs-lookup"><span data-stu-id="990d8-116">PARAMETERS</span></span>

### <span data-ttu-id="990d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990d8-117">-DefaultProfile</span></span>
<span data-ttu-id="990d8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="990d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="990d8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="990d8-119">-InputObject</span></span>
<span data-ttu-id="990d8-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="990d8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="990d8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="990d8-121">-Name</span></span>
<span data-ttu-id="990d8-122">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="990d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="990d8-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="990d8-124">The name of the resource group.</span></span>
<span data-ttu-id="990d8-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="990d8-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="990d8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="990d8-126">-SubscriptionId</span></span>
<span data-ttu-id="990d8-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="990d8-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="990d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990d8-128">CommonParameters</span></span>
<span data-ttu-id="990d8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="990d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990d8-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="990d8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990d8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="990d8-131">INPUTS</span></span>

### <span data-ttu-id="990d8-132">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="990d8-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="990d8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="990d8-133">OUTPUTS</span></span>

### <span data-ttu-id="990d8-134">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="990d8-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="990d8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="990d8-135">NOTES</span></span>

<span data-ttu-id="990d8-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="990d8-136">ALIASES</span></span>

<span data-ttu-id="990d8-137">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="990d8-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="990d8-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="990d8-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="990d8-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="990d8-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="990d8-140">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="990d8-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="990d8-141">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="990d8-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="990d8-142">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="990d8-143">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="990d8-144">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="990d8-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="990d8-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="990d8-146">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="990d8-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="990d8-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="990d8-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="990d8-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="990d8-149">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="990d8-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="990d8-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="990d8-151">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="990d8-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="990d8-152">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="990d8-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="990d8-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="990d8-153">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116846"
---
# <span data-ttu-id="17591-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="17591-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="17591-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17591-102">SYNOPSIS</span></span>
<span data-ttu-id="17591-103">Obter um pool de host.</span><span class="sxs-lookup"><span data-stu-id="17591-103">Get a host pool.</span></span>

## <span data-ttu-id="17591-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17591-104">SYNTAX</span></span>

### <span data-ttu-id="17591-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17591-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17591-106">Obter</span><span class="sxs-lookup"><span data-stu-id="17591-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17591-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17591-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="17591-108">Lista</span><span class="sxs-lookup"><span data-stu-id="17591-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="17591-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="17591-109">DESCRIPTION</span></span>
<span data-ttu-id="17591-110">Obter um pool de host.</span><span class="sxs-lookup"><span data-stu-id="17591-110">Get a host pool.</span></span>

## <span data-ttu-id="17591-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17591-111">EXAMPLES</span></span>

### <span data-ttu-id="17591-112">Exemplo 1: Obter um HostPool da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="17591-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="17591-113">Esse comando obtém um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="17591-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="17591-114">Exemplo 2: Listar HostPools da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="17591-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="17591-115">Esse comando lista um HostPools da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="17591-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="17591-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17591-116">PARAMETERS</span></span>

### <span data-ttu-id="17591-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17591-117">-DefaultProfile</span></span>
<span data-ttu-id="17591-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17591-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17591-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17591-119">-InputObject</span></span>
<span data-ttu-id="17591-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="17591-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17591-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="17591-121">-Name</span></span>
<span data-ttu-id="17591-122">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="17591-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="17591-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17591-123">-ResourceGroupName</span></span>
<span data-ttu-id="17591-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17591-124">The name of the resource group.</span></span>
<span data-ttu-id="17591-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="17591-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="17591-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17591-126">-SubscriptionId</span></span>
<span data-ttu-id="17591-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="17591-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="17591-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17591-128">CommonParameters</span></span>
<span data-ttu-id="17591-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17591-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17591-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17591-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17591-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="17591-131">INPUTS</span></span>

### <span data-ttu-id="17591-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="17591-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="17591-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="17591-133">OUTPUTS</span></span>

### <span data-ttu-id="17591-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="17591-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="17591-135">Notas</span><span class="sxs-lookup"><span data-stu-id="17591-135">NOTES</span></span>

<span data-ttu-id="17591-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="17591-136">ALIASES</span></span>

<span data-ttu-id="17591-137">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="17591-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17591-138">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="17591-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17591-139">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17591-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17591-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="17591-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17591-141">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="17591-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="17591-142">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="17591-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="17591-143">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="17591-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="17591-144">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="17591-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="17591-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="17591-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17591-146">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="17591-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="17591-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17591-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="17591-148">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="17591-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="17591-149">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="17591-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="17591-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="17591-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="17591-151">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="17591-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="17591-152">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="17591-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="17591-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17591-153">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115348"
---
# <span data-ttu-id="1b170-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="1b170-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="1b170-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b170-102">SYNOPSIS</span></span>
<span data-ttu-id="1b170-103">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b170-103">Get a desktop.</span></span>

## <span data-ttu-id="1b170-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b170-104">SYNTAX</span></span>

### <span data-ttu-id="1b170-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b170-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b170-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1b170-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b170-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b170-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b170-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b170-108">DESCRIPTION</span></span>
<span data-ttu-id="1b170-109">Obter uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b170-109">Get a desktop.</span></span>

## <span data-ttu-id="1b170-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b170-110">EXAMPLES</span></span>

### <span data-ttu-id="1b170-111">Exemplo 1: Obter uma Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="1b170-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="1b170-112">Esse comando obtém uma Área de Trabalho Virtual do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1b170-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="1b170-113">Exemplo 2: Listar áreas de trabalho virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="1b170-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="1b170-114">Este comando lista As Áreas de Trabalho Virtuais daWindows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1b170-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="1b170-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b170-115">PARAMETERS</span></span>

### <span data-ttu-id="1b170-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="1b170-116">-ApplicationGroupName</span></span>
<span data-ttu-id="1b170-117">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="1b170-117">The name of the application group</span></span>

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

### <span data-ttu-id="1b170-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b170-118">-DefaultProfile</span></span>
<span data-ttu-id="1b170-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b170-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b170-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b170-120">-InputObject</span></span>
<span data-ttu-id="1b170-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1b170-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b170-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b170-122">-Name</span></span>
<span data-ttu-id="1b170-123">O nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="1b170-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b170-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b170-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b170-125">The name of the resource group.</span></span>
<span data-ttu-id="1b170-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b170-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1b170-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b170-127">-SubscriptionId</span></span>
<span data-ttu-id="1b170-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1b170-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1b170-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b170-129">CommonParameters</span></span>
<span data-ttu-id="1b170-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b170-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b170-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b170-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b170-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="1b170-132">INPUTS</span></span>

### <span data-ttu-id="1b170-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1b170-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1b170-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1b170-134">OUTPUTS</span></span>

### <span data-ttu-id="1b170-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="1b170-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="1b170-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="1b170-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="1b170-137">Notas</span><span class="sxs-lookup"><span data-stu-id="1b170-137">NOTES</span></span>

<span data-ttu-id="1b170-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="1b170-138">ALIASES</span></span>

<span data-ttu-id="1b170-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="1b170-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b170-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1b170-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b170-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b170-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b170-142">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="1b170-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b170-143">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="1b170-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1b170-144">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1b170-145">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1b170-146">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1b170-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="1b170-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b170-148">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1b170-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b170-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1b170-150">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b170-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="1b170-151">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1b170-152">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1b170-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1b170-153">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="1b170-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1b170-154">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1b170-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1b170-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b170-155">RELATED LINKS</span></span>


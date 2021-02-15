---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111921"
---
# <span data-ttu-id="c199d-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c199d-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="c199d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c199d-102">SYNOPSIS</span></span>
<span data-ttu-id="c199d-103">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c199d-103">Get an application group.</span></span>

## <span data-ttu-id="c199d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c199d-104">SYNTAX</span></span>

### <span data-ttu-id="c199d-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c199d-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c199d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c199d-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c199d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c199d-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c199d-108">Lista</span><span class="sxs-lookup"><span data-stu-id="c199d-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c199d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c199d-109">DESCRIPTION</span></span>
<span data-ttu-id="c199d-110">Obter um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c199d-110">Get an application group.</span></span>

## <span data-ttu-id="c199d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c199d-111">EXAMPLES</span></span>

### <span data-ttu-id="c199d-112">Exemplo 1: Obter um Grupo de Aplicativos da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="c199d-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c199d-113">Esse comando obtém um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c199d-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="c199d-114">Exemplo 2: Listar Grupos de Aplicativos da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="c199d-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="c199d-115">Esse comando lista um Grupo de Aplicativos da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c199d-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="c199d-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c199d-116">PARAMETERS</span></span>

### <span data-ttu-id="c199d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c199d-117">-DefaultProfile</span></span>
<span data-ttu-id="c199d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c199d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c199d-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c199d-119">-Filter</span></span>
<span data-ttu-id="c199d-120">Expressão de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c199d-120">OData filter expression.</span></span>
<span data-ttu-id="c199d-121">As propriedades válidas para filtragem são applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="c199d-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c199d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c199d-122">-InputObject</span></span>
<span data-ttu-id="c199d-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c199d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c199d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c199d-124">-Name</span></span>
<span data-ttu-id="c199d-125">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c199d-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c199d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c199d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c199d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c199d-127">The name of the resource group.</span></span>
<span data-ttu-id="c199d-128">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c199d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c199d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c199d-129">-SubscriptionId</span></span>
<span data-ttu-id="c199d-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c199d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c199d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c199d-131">CommonParameters</span></span>
<span data-ttu-id="c199d-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c199d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c199d-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c199d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c199d-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="c199d-134">INPUTS</span></span>

### <span data-ttu-id="c199d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c199d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c199d-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="c199d-136">OUTPUTS</span></span>

### <span data-ttu-id="c199d-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="c199d-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="c199d-138">Notas</span><span class="sxs-lookup"><span data-stu-id="c199d-138">NOTES</span></span>

<span data-ttu-id="c199d-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="c199d-139">ALIASES</span></span>

<span data-ttu-id="c199d-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="c199d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c199d-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c199d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c199d-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c199d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c199d-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="c199d-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c199d-144">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c199d-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c199d-145">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c199d-146">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c199d-147">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c199d-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c199d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c199d-149">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c199d-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c199d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c199d-151">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c199d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="c199d-152">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c199d-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c199d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c199d-154">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="c199d-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c199d-155">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c199d-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c199d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c199d-156">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 67a49250607e1c7d70f1799aa26bd866924b5edc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116845"
---
# <span data-ttu-id="ee1cd-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="ee1cd-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="ee1cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1cd-103">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-103">Get an application.</span></span>

## <span data-ttu-id="ee1cd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee1cd-104">SYNTAX</span></span>

### <span data-ttu-id="ee1cd-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee1cd-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1cd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ee1cd-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee1cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1cd-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee1cd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee1cd-108">DESCRIPTION</span></span>
<span data-ttu-id="ee1cd-109">Obter um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-109">Get an application.</span></span>

## <span data-ttu-id="ee1cd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee1cd-110">EXAMPLES</span></span>

### <span data-ttu-id="ee1cd-111">Exemplo 1: Obter um aplicativo virtual da área de trabalho do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="ee1cd-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="ee1cd-112">Esse comando obtém um Aplicativo virtual da área de trabalho do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="ee1cd-113">Exemplo 2: Listar aplicativos de área de trabalho virtuais do Windows</span><span class="sxs-lookup"><span data-stu-id="ee1cd-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="ee1cd-114">Este comando lista aplicativos de área de trabalho virtuais do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="ee1cd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee1cd-115">PARAMETERS</span></span>

### <span data-ttu-id="ee1cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1cd-116">-DefaultProfile</span></span>
<span data-ttu-id="ee1cd-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1cd-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="ee1cd-118">-GroupName</span></span>
<span data-ttu-id="ee1cd-119">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ee1cd-119">The name of the application group</span></span>

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

### <span data-ttu-id="ee1cd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1cd-120">-InputObject</span></span>
<span data-ttu-id="ee1cd-121">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee1cd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee1cd-122">-Name</span></span>
<span data-ttu-id="ee1cd-123">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="ee1cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee1cd-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-125">The name of the resource group.</span></span>
<span data-ttu-id="ee1cd-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ee1cd-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee1cd-127">-SubscriptionId</span></span>
<span data-ttu-id="ee1cd-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ee1cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1cd-129">CommonParameters</span></span>
<span data-ttu-id="ee1cd-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1cd-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee1cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1cd-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee1cd-132">INPUTS</span></span>

### <span data-ttu-id="ee1cd-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ee1cd-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ee1cd-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee1cd-134">OUTPUTS</span></span>

### <span data-ttu-id="ee1cd-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="ee1cd-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="ee1cd-136">Notas</span><span class="sxs-lookup"><span data-stu-id="ee1cd-136">NOTES</span></span>

<span data-ttu-id="ee1cd-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="ee1cd-137">ALIASES</span></span>

<span data-ttu-id="ee1cd-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ee1cd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee1cd-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee1cd-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee1cd-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="ee1cd-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee1cd-142">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ee1cd-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ee1cd-143">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ee1cd-144">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ee1cd-145">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ee1cd-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ee1cd-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee1cd-147">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ee1cd-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ee1cd-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="ee1cd-150">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ee1cd-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ee1cd-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ee1cd-152">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="ee1cd-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ee1cd-153">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ee1cd-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ee1cd-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee1cd-154">RELATED LINKS</span></span>


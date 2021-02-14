---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116844"
---
# <span data-ttu-id="a7301-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a7301-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="a7301-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7301-102">SYNOPSIS</span></span>
<span data-ttu-id="a7301-103">Obter uma msixpackage.</span><span class="sxs-lookup"><span data-stu-id="a7301-103">Get a msixpackage.</span></span>

## <span data-ttu-id="a7301-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7301-104">SYNTAX</span></span>

### <span data-ttu-id="a7301-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7301-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7301-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a7301-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7301-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7301-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7301-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7301-108">DESCRIPTION</span></span>
<span data-ttu-id="a7301-109">Obter uma msixpackage.</span><span class="sxs-lookup"><span data-stu-id="a7301-109">Get a msixpackage.</span></span>

## <span data-ttu-id="a7301-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7301-110">EXAMPLES</span></span>

### <span data-ttu-id="a7301-111">Exemplo 1: Obter um Pacote MSIX por Nome</span><span class="sxs-lookup"><span data-stu-id="a7301-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a7301-112">Esse comando obtém um Pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="a7301-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="a7301-113">Exemplo 2: Listar pacotes MSIX</span><span class="sxs-lookup"><span data-stu-id="a7301-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a7301-114">Este comando lista pacotes MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="a7301-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="a7301-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7301-115">PARAMETERS</span></span>

### <span data-ttu-id="a7301-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7301-116">-DefaultProfile</span></span>
<span data-ttu-id="a7301-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7301-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7301-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="a7301-118">-FullName</span></span>
<span data-ttu-id="a7301-119">O nome completo do pacote de versão específico do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7301-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a7301-120">-HostPoolName</span></span>
<span data-ttu-id="a7301-121">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a7301-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7301-122">-InputObject</span></span>
<span data-ttu-id="a7301-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a7301-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7301-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7301-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7301-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7301-125">The name of the resource group.</span></span>
<span data-ttu-id="a7301-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7301-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a7301-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7301-127">-SubscriptionId</span></span>
<span data-ttu-id="a7301-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a7301-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a7301-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7301-129">CommonParameters</span></span>
<span data-ttu-id="a7301-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7301-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7301-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7301-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7301-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7301-132">INPUTS</span></span>

### <span data-ttu-id="a7301-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a7301-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a7301-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7301-134">OUTPUTS</span></span>

### <span data-ttu-id="a7301-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a7301-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="a7301-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a7301-136">NOTES</span></span>

<span data-ttu-id="a7301-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="a7301-137">ALIASES</span></span>

<span data-ttu-id="a7301-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a7301-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7301-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a7301-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7301-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7301-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7301-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a7301-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7301-142">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a7301-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a7301-143">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a7301-144">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a7301-145">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a7301-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a7301-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7301-147">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a7301-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7301-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a7301-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7301-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7301-150">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a7301-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a7301-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a7301-152">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a7301-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a7301-153">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a7301-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a7301-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7301-154">RELATED LINKS</span></span>


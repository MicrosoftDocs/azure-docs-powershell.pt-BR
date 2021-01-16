---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272909"
---
# <span data-ttu-id="63cd4-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="63cd4-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="63cd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="63cd4-103">Obtenha um msixpackage.</span><span class="sxs-lookup"><span data-stu-id="63cd4-103">Get a msixpackage.</span></span>

## <span data-ttu-id="63cd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63cd4-104">SYNTAX</span></span>

### <span data-ttu-id="63cd4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="63cd4-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="63cd4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="63cd4-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="63cd4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="63cd4-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="63cd4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63cd4-108">DESCRIPTION</span></span>
<span data-ttu-id="63cd4-109">Obtenha um msixpackage.</span><span class="sxs-lookup"><span data-stu-id="63cd4-109">Get a msixpackage.</span></span>

## <span data-ttu-id="63cd4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63cd4-110">EXAMPLES</span></span>

### <span data-ttu-id="63cd4-111">Exemplo 1: obter um pacote MSIX por nome</span><span class="sxs-lookup"><span data-stu-id="63cd4-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="63cd4-112">Esse comando obtém um pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="63cd4-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="63cd4-113">Exemplo 2: list MSIX Packages</span><span class="sxs-lookup"><span data-stu-id="63cd4-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="63cd4-114">Esse comando lista os pacotes MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="63cd4-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="63cd4-115">OS</span><span class="sxs-lookup"><span data-stu-id="63cd4-115">PARAMETERS</span></span>

### <span data-ttu-id="63cd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cd4-116">-DefaultProfile</span></span>
<span data-ttu-id="63cd4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63cd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63cd4-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="63cd4-118">-FullName</span></span>
<span data-ttu-id="63cd4-119">O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="63cd4-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="63cd4-120">-HostPoolName</span></span>
<span data-ttu-id="63cd4-121">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="63cd4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63cd4-122">-InputObject</span></span>
<span data-ttu-id="63cd4-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="63cd4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="63cd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="63cd4-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63cd4-125">The name of the resource group.</span></span>
<span data-ttu-id="63cd4-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="63cd4-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="63cd4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63cd4-127">-SubscriptionId</span></span>
<span data-ttu-id="63cd4-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="63cd4-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="63cd4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cd4-129">CommonParameters</span></span>
<span data-ttu-id="63cd4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cd4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cd4-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63cd4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cd4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63cd4-132">INPUTS</span></span>

### <span data-ttu-id="63cd4-133">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="63cd4-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="63cd4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63cd4-134">OUTPUTS</span></span>

### <span data-ttu-id="63cd4-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="63cd4-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="63cd4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63cd4-136">NOTES</span></span>

<span data-ttu-id="63cd4-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="63cd4-137">ALIASES</span></span>

<span data-ttu-id="63cd4-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="63cd4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63cd4-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="63cd4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63cd4-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63cd4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63cd4-141">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="63cd4-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63cd4-142">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="63cd4-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="63cd4-143">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="63cd4-144">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="63cd4-145">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="63cd4-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="63cd4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63cd4-147">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="63cd4-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63cd4-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="63cd4-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="63cd4-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="63cd4-150">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="63cd4-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="63cd4-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="63cd4-152">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="63cd4-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="63cd4-153">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="63cd4-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="63cd4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63cd4-154">RELATED LINKS</span></span>


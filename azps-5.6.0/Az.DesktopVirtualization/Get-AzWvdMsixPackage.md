---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 942b0cc6dc00d80eb56748de09c8818045dfca40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888957"
---
# <span data-ttu-id="3bf10-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3bf10-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="3bf10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bf10-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf10-103">Obter um msixpackage.</span><span class="sxs-lookup"><span data-stu-id="3bf10-103">Get a msixpackage.</span></span>

## <span data-ttu-id="3bf10-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3bf10-104">SYNTAX</span></span>

### <span data-ttu-id="3bf10-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3bf10-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bf10-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3bf10-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bf10-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bf10-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bf10-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3bf10-108">DESCRIPTION</span></span>
<span data-ttu-id="3bf10-109">Obter um msixpackage.</span><span class="sxs-lookup"><span data-stu-id="3bf10-109">Get a msixpackage.</span></span>

## <span data-ttu-id="3bf10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3bf10-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf10-111">Exemplo 1: Obter um pacote MSIX pelo nome</span><span class="sxs-lookup"><span data-stu-id="3bf10-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="3bf10-112">Este comando obtém um Pacote MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="3bf10-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="3bf10-113">Exemplo 2: Listar pacotes MSIX</span><span class="sxs-lookup"><span data-stu-id="3bf10-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="3bf10-114">Este comando lista pacotes MSIX em um HostPool.</span><span class="sxs-lookup"><span data-stu-id="3bf10-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="3bf10-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3bf10-115">PARAMETERS</span></span>

### <span data-ttu-id="3bf10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf10-116">-DefaultProfile</span></span>
<span data-ttu-id="3bf10-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bf10-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="3bf10-118">-FullName</span></span>
<span data-ttu-id="3bf10-119">O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="3bf10-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3bf10-120">-HostPoolName</span></span>
<span data-ttu-id="3bf10-121">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3bf10-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bf10-122">-InputObject</span></span>
<span data-ttu-id="3bf10-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3bf10-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bf10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf10-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bf10-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3bf10-125">The name of the resource group.</span></span>
<span data-ttu-id="3bf10-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3bf10-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3bf10-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bf10-127">-SubscriptionId</span></span>
<span data-ttu-id="3bf10-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3bf10-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3bf10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf10-129">CommonParameters</span></span>
<span data-ttu-id="3bf10-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf10-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bf10-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf10-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bf10-132">INPUTS</span></span>

### <span data-ttu-id="3bf10-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3bf10-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3bf10-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3bf10-134">OUTPUTS</span></span>

### <span data-ttu-id="3bf10-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3bf10-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="3bf10-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3bf10-136">NOTES</span></span>

<span data-ttu-id="3bf10-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3bf10-137">ALIASES</span></span>

<span data-ttu-id="3bf10-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="3bf10-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bf10-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3bf10-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bf10-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bf10-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bf10-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="3bf10-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bf10-142">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3bf10-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3bf10-143">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3bf10-144">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3bf10-145">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3bf10-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3bf10-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bf10-147">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3bf10-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3bf10-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3bf10-149">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3bf10-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3bf10-150">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3bf10-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3bf10-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3bf10-152">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="3bf10-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3bf10-153">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3bf10-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3bf10-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bf10-154">RELATED LINKS</span></span>


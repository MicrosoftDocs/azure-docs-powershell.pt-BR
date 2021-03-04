---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: f4767b87e7230727a2cf9c83af0c2aa5d03b908a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887160"
---
# <span data-ttu-id="0c3a5-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="0c3a5-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="0c3a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3a5-103">Expande e lista pacotes MSIX em uma Imagem, considerando o Caminho da Imagem.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="0c3a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c3a5-104">SYNTAX</span></span>

### <span data-ttu-id="0c3a5-105">ExpandExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0c3a5-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c3a5-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="0c3a5-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c3a5-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0c3a5-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0c3a5-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0c3a5-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c3a5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c3a5-109">DESCRIPTION</span></span>
<span data-ttu-id="0c3a5-110">Expande e lista pacotes MSIX em uma Imagem, considerando o Caminho da Imagem.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="0c3a5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-111">EXAMPLES</span></span>

### <span data-ttu-id="0c3a5-112">Exemplo 1: expande o Caminho da Imagem especificado e recupera os metadados do pacote encontrados no AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="0c3a5-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="0c3a5-113">Este comando retorna metadados do pacote MSIX encontrados no caminho de imagem determinado.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="0c3a5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-114">PARAMETERS</span></span>

### <span data-ttu-id="0c3a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3a5-115">-DefaultProfile</span></span>
<span data-ttu-id="0c3a5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3a5-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0c3a5-117">-HostPoolName</span></span>
<span data-ttu-id="0c3a5-118">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3a5-119">-InputObject</span></span>
<span data-ttu-id="0c3a5-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="0c3a5-121">-MsixImageUri</span></span>
<span data-ttu-id="0c3a5-122">Representa o URI referente à MSIX Image To construct, consulte a seção NOTES para propriedades MSIXIMAGEURI e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c3a5-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-124">The name of the resource group.</span></span>
<span data-ttu-id="0c3a5-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c3a5-126">-SubscriptionId</span></span>
<span data-ttu-id="0c3a5-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="0c3a5-128">-Uri</span></span>
<span data-ttu-id="0c3a5-129">URI para Imagem</span><span class="sxs-lookup"><span data-stu-id="0c3a5-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c3a5-130">-Confirm</span></span>
<span data-ttu-id="0c3a5-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3a5-132">-WhatIf</span></span>
<span data-ttu-id="0c3a5-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3a5-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3a5-135">CommonParameters</span></span>
<span data-ttu-id="0c3a5-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3a5-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c3a5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3a5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-138">INPUTS</span></span>

### <span data-ttu-id="0c3a5-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="0c3a5-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="0c3a5-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0c3a5-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0c3a5-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-141">OUTPUTS</span></span>

### <span data-ttu-id="0c3a5-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="0c3a5-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="0c3a5-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c3a5-143">NOTES</span></span>

<span data-ttu-id="0c3a5-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0c3a5-144">ALIASES</span></span>

<span data-ttu-id="0c3a5-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="0c3a5-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0c3a5-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c3a5-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0c3a5-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="0c3a5-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c3a5-149">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="0c3a5-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0c3a5-150">`[ApplicationName <String>]`: O nome do aplicativo no grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0c3a5-151">`[DesktopName <String>]`: O nome da área de trabalho no grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0c3a5-152">`[HostPoolName <String>]`: O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0c3a5-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0c3a5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c3a5-154">`[MsixPackageFullName <String>]`: O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0c3a5-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0c3a5-156">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="0c3a5-157">`[SessionHostName <String>]`: O nome do host da sessão no pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0c3a5-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0c3a5-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0c3a5-159">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="0c3a5-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0c3a5-160">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0c3a5-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="0c3a5-161">MSIXIMAGEURI <IMsixImageUri> : representa URI referente à imagem MSIX</span><span class="sxs-lookup"><span data-stu-id="0c3a5-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="0c3a5-162">`[Uri <String>]`: URI para Imagem</span><span class="sxs-lookup"><span data-stu-id="0c3a5-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="0c3a5-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c3a5-163">RELATED LINKS</span></span>


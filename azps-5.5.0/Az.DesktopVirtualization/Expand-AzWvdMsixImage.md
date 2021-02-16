---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113235"
---
# <span data-ttu-id="faa4d-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="faa4d-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="faa4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faa4d-102">SYNOPSIS</span></span>
<span data-ttu-id="faa4d-103">Expande e lista pacotes MSIX em uma Imagem, de acordo com o Caminho da Imagem.</span><span class="sxs-lookup"><span data-stu-id="faa4d-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="faa4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faa4d-104">SYNTAX</span></span>

### <span data-ttu-id="faa4d-105">ExpandExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="faa4d-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faa4d-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="faa4d-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faa4d-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="faa4d-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faa4d-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="faa4d-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faa4d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="faa4d-109">DESCRIPTION</span></span>
<span data-ttu-id="faa4d-110">Expande e lista pacotes MSIX em uma Imagem, de acordo com o Caminho da Imagem.</span><span class="sxs-lookup"><span data-stu-id="faa4d-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="faa4d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="faa4d-111">EXAMPLES</span></span>

### <span data-ttu-id="faa4d-112">Exemplo 1: expande o Caminho da Imagem especificado e recupera metadados de pacote encontrados no AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="faa4d-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="faa4d-113">Esse comando retorna Metadados do Pacote MSIX encontrados no Caminho da Imagem determinado.</span><span class="sxs-lookup"><span data-stu-id="faa4d-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="faa4d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faa4d-114">PARAMETERS</span></span>

### <span data-ttu-id="faa4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa4d-115">-DefaultProfile</span></span>
<span data-ttu-id="faa4d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faa4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa4d-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="faa4d-117">-HostPoolName</span></span>
<span data-ttu-id="faa4d-118">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="faa4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa4d-119">-InputObject</span></span>
<span data-ttu-id="faa4d-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="faa4d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="faa4d-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="faa4d-121">-MsixImageUri</span></span>
<span data-ttu-id="faa4d-122">Representa URI que faz referência à imagem MSIX Para construir, confira a seção ANOTAÇÕES para as propriedades MSIXIMAGEURI e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="faa4d-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="faa4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="faa4d-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faa4d-124">The name of the resource group.</span></span>
<span data-ttu-id="faa4d-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="faa4d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="faa4d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faa4d-126">-SubscriptionId</span></span>
<span data-ttu-id="faa4d-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="faa4d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="faa4d-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="faa4d-128">-Uri</span></span>
<span data-ttu-id="faa4d-129">URI para Imagem</span><span class="sxs-lookup"><span data-stu-id="faa4d-129">URI to Image</span></span>

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

### <span data-ttu-id="faa4d-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="faa4d-130">-Confirm</span></span>
<span data-ttu-id="faa4d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa4d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa4d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa4d-132">-WhatIf</span></span>
<span data-ttu-id="faa4d-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="faa4d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa4d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="faa4d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa4d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa4d-135">CommonParameters</span></span>
<span data-ttu-id="faa4d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa4d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa4d-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faa4d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa4d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="faa4d-138">INPUTS</span></span>

### <span data-ttu-id="faa4d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="faa4d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="faa4d-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="faa4d-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="faa4d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="faa4d-141">OUTPUTS</span></span>

### <span data-ttu-id="faa4d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="faa4d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="faa4d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="faa4d-143">NOTES</span></span>

<span data-ttu-id="faa4d-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="faa4d-144">ALIASES</span></span>

<span data-ttu-id="faa4d-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="faa4d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="faa4d-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="faa4d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="faa4d-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="faa4d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="faa4d-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="faa4d-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="faa4d-149">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="faa4d-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="faa4d-150">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="faa4d-151">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="faa4d-152">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="faa4d-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="faa4d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="faa4d-154">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="faa4d-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faa4d-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="faa4d-156">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="faa4d-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="faa4d-157">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="faa4d-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="faa4d-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="faa4d-159">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="faa4d-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="faa4d-160">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="faa4d-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="faa4d-161">MSIXIMAGEURI <IMsixImageUri> : representa URI que faz referência à imagem MSIX</span><span class="sxs-lookup"><span data-stu-id="faa4d-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="faa4d-162">`[Uri <String>]`: URI para Imagem</span><span class="sxs-lookup"><span data-stu-id="faa4d-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="faa4d-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faa4d-163">RELATED LINKS</span></span>


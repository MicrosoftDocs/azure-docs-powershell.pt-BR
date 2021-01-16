---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 417acf03af2bf73d57759841bacc3ed532e8f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260737"
---
# <span data-ttu-id="a2f6d-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="a2f6d-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="a2f6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f6d-103">Expande e lista pacotes MSIX em uma imagem, considerando-se o caminho da imagem.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a2f6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2f6d-104">SYNTAX</span></span>

### <span data-ttu-id="a2f6d-105">ExpandExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2f6d-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2f6d-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="a2f6d-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2f6d-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2f6d-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2f6d-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a2f6d-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2f6d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2f6d-109">DESCRIPTION</span></span>
<span data-ttu-id="a2f6d-110">Expande e lista pacotes MSIX em uma imagem, considerando-se o caminho da imagem.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a2f6d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2f6d-111">EXAMPLES</span></span>

### <span data-ttu-id="a2f6d-112">Exemplo 1: expande o caminho da imagem especificada e recupera os metadados do pacote encontrados no AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a2f6d-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="a2f6d-113">Esse comando retorna metadados do pacote MSIX localizado no caminho de imagem fornecido.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="a2f6d-114">OS</span><span class="sxs-lookup"><span data-stu-id="a2f6d-114">PARAMETERS</span></span>

### <span data-ttu-id="a2f6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f6d-115">-DefaultProfile</span></span>
<span data-ttu-id="a2f6d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f6d-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a2f6d-117">-HostPoolName</span></span>
<span data-ttu-id="a2f6d-118">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a2f6d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f6d-119">-InputObject</span></span>
<span data-ttu-id="a2f6d-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2f6d-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a2f6d-121">-MsixImageUri</span></span>
<span data-ttu-id="a2f6d-122">Representa o URI que faz referência a uma imagem do MSIX para construir, consulte a seção notas para propriedades de MSIXIMAGEURI e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2f6d-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-124">The name of the resource group.</span></span>
<span data-ttu-id="a2f6d-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a2f6d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2f6d-126">-SubscriptionId</span></span>
<span data-ttu-id="a2f6d-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a2f6d-128">-URI</span><span class="sxs-lookup"><span data-stu-id="a2f6d-128">-Uri</span></span>
<span data-ttu-id="a2f6d-129">URI para imagem</span><span class="sxs-lookup"><span data-stu-id="a2f6d-129">URI to Image</span></span>

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

### <span data-ttu-id="a2f6d-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2f6d-130">-Confirm</span></span>
<span data-ttu-id="a2f6d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f6d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f6d-132">-WhatIf</span></span>
<span data-ttu-id="a2f6d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f6d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f6d-135">CommonParameters</span></span>
<span data-ttu-id="a2f6d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f6d-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2f6d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f6d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2f6d-138">INPUTS</span></span>

### <span data-ttu-id="a2f6d-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a2f6d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span></span>

### <span data-ttu-id="a2f6d-140">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a2f6d-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a2f6d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2f6d-141">OUTPUTS</span></span>

### <span data-ttu-id="a2f6d-142">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="a2f6d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="a2f6d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2f6d-143">NOTES</span></span>

<span data-ttu-id="a2f6d-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a2f6d-144">ALIASES</span></span>

<span data-ttu-id="a2f6d-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a2f6d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2f6d-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2f6d-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2f6d-148">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a2f6d-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2f6d-149">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a2f6d-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a2f6d-150">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a2f6d-151">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a2f6d-152">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a2f6d-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a2f6d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2f6d-154">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a2f6d-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a2f6d-156">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a2f6d-157">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a2f6d-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a2f6d-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a2f6d-159">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="a2f6d-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a2f6d-160">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a2f6d-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="a2f6d-161">MSIXIMAGEURI <IMsixImageUri> : representa o URI que faz referência à imagem MSIX</span><span class="sxs-lookup"><span data-stu-id="a2f6d-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="a2f6d-162">`[Uri <String>]`: URI para Image</span><span class="sxs-lookup"><span data-stu-id="a2f6d-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="a2f6d-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2f6d-163">RELATED LINKS</span></span>


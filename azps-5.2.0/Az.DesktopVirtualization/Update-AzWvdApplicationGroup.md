---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: 239d1a5a38d2eb344f584e006d465598b43dd546
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259559"
---
# <span data-ttu-id="5588d-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5588d-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="5588d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5588d-102">SYNOPSIS</span></span>
<span data-ttu-id="5588d-103">Atualize um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5588d-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="5588d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5588d-104">SYNTAX</span></span>

### <span data-ttu-id="5588d-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="5588d-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5588d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5588d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5588d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5588d-107">DESCRIPTION</span></span>
<span data-ttu-id="5588d-108">Atualize um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5588d-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="5588d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5588d-109">EXAMPLES</span></span>

### <span data-ttu-id="5588d-110">Exemplo 1: criar um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="5588d-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5588d-111">Esse comando cria um grupo de aplicativos área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5588d-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="5588d-112">OS</span><span class="sxs-lookup"><span data-stu-id="5588d-112">PARAMETERS</span></span>

### <span data-ttu-id="5588d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5588d-113">-DefaultProfile</span></span>
<span data-ttu-id="5588d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5588d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5588d-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5588d-115">-Description</span></span>
<span data-ttu-id="5588d-116">Descrição do FileApp.</span><span class="sxs-lookup"><span data-stu-id="5588d-116">Description of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5588d-117">-FriendlyName</span></span>
<span data-ttu-id="5588d-118">Nome amigável do nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5588d-118">Friendly name of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5588d-119">-InputObject</span></span>
<span data-ttu-id="5588d-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5588d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5588d-121">-Name</span></span>
<span data-ttu-id="5588d-122">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="5588d-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5588d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5588d-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5588d-124">The name of the resource group.</span></span>
<span data-ttu-id="5588d-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5588d-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5588d-126">-SubscriptionId</span></span>
<span data-ttu-id="5588d-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5588d-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="5588d-128">-Tag</span></span>
<span data-ttu-id="5588d-129">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="5588d-129">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5588d-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5588d-130">-Confirm</span></span>
<span data-ttu-id="5588d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5588d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5588d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5588d-132">-WhatIf</span></span>
<span data-ttu-id="5588d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5588d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5588d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5588d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5588d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5588d-135">CommonParameters</span></span>
<span data-ttu-id="5588d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5588d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5588d-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5588d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5588d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5588d-138">INPUTS</span></span>

### <span data-ttu-id="5588d-139">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5588d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5588d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5588d-140">OUTPUTS</span></span>

### <span data-ttu-id="5588d-141">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5588d-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="5588d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5588d-142">NOTES</span></span>

<span data-ttu-id="5588d-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5588d-143">ALIASES</span></span>

<span data-ttu-id="5588d-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5588d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5588d-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5588d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5588d-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5588d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5588d-147">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5588d-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5588d-148">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="5588d-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5588d-149">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5588d-150">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5588d-151">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5588d-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5588d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5588d-153">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5588d-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5588d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5588d-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5588d-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="5588d-156">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5588d-157">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5588d-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5588d-158">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="5588d-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5588d-159">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5588d-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5588d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5588d-160">RELATED LINKS</span></span>


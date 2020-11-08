---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117488"
---
# <span data-ttu-id="36e0e-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="36e0e-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="36e0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="36e0e-103">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-103">Update an application.</span></span>

## <span data-ttu-id="36e0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36e0e-104">SYNTAX</span></span>

### <span data-ttu-id="36e0e-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="36e0e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="36e0e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36e0e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36e0e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36e0e-107">DESCRIPTION</span></span>
<span data-ttu-id="36e0e-108">Atualizar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-108">Update an application.</span></span>

## <span data-ttu-id="36e0e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36e0e-109">EXAMPLES</span></span>

### <span data-ttu-id="36e0e-110">Exemplo 1: atualizar um aplicativo de área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="36e0e-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="36e0e-111">Esse comando atualiza um aplicativo de área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="36e0e-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="36e0e-112">OS</span><span class="sxs-lookup"><span data-stu-id="36e0e-112">PARAMETERS</span></span>

### <span data-ttu-id="36e0e-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="36e0e-113">-CommandLineArgument</span></span>
<span data-ttu-id="36e0e-114">Argumentos de linha de comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="36e0e-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="36e0e-115">-CommandLineSetting</span></span>
<span data-ttu-id="36e0e-116">Especifica se esse aplicativo publicado pode ser iniciado com argumentos de linha de comando fornecidos pelo cliente, argumentos de linha de comando especificados no tempo de publicação ou nenhum argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="36e0e-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e0e-117">-DefaultProfile</span></span>
<span data-ttu-id="36e0e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36e0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e0e-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="36e0e-119">-Description</span></span>
<span data-ttu-id="36e0e-120">Descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-120">Description of Application.</span></span>

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

### <span data-ttu-id="36e0e-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="36e0e-121">-FilePath</span></span>
<span data-ttu-id="36e0e-122">Especifica um caminho para o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="36e0e-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="36e0e-123">-FriendlyName</span></span>
<span data-ttu-id="36e0e-124">Nome amigável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e0e-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="36e0e-125">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="36e0e-125">-GroupName</span></span>
<span data-ttu-id="36e0e-126">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="36e0e-126">The name of the application group</span></span>

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

### <span data-ttu-id="36e0e-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="36e0e-127">-IconIndex</span></span>
<span data-ttu-id="36e0e-128">Índice do ícone.</span><span class="sxs-lookup"><span data-stu-id="36e0e-128">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e0e-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="36e0e-129">-IconPath</span></span>
<span data-ttu-id="36e0e-130">Caminho para o ícone.</span><span class="sxs-lookup"><span data-stu-id="36e0e-130">Path to icon.</span></span>

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

### <span data-ttu-id="36e0e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e0e-131">-InputObject</span></span>
<span data-ttu-id="36e0e-132">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="36e0e-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36e0e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="36e0e-133">-Name</span></span>
<span data-ttu-id="36e0e-134">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e0e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e0e-135">-ResourceGroupName</span></span>
<span data-ttu-id="36e0e-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36e0e-136">The name of the resource group.</span></span>
<span data-ttu-id="36e0e-137">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="36e0e-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36e0e-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="36e0e-138">-ShowInPortal</span></span>
<span data-ttu-id="36e0e-139">Especifica se o programa RemoteApp deve ser mostrado no servidor de acesso à Web da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="36e0e-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e0e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36e0e-140">-SubscriptionId</span></span>
<span data-ttu-id="36e0e-141">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="36e0e-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36e0e-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="36e0e-142">-Tag</span></span>
<span data-ttu-id="36e0e-143">marcas a serem atualizadas</span><span class="sxs-lookup"><span data-stu-id="36e0e-143">tags to be updated</span></span>

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

### <span data-ttu-id="36e0e-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36e0e-144">-Confirm</span></span>
<span data-ttu-id="36e0e-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e0e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e0e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e0e-146">-WhatIf</span></span>
<span data-ttu-id="36e0e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36e0e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e0e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36e0e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e0e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e0e-149">CommonParameters</span></span>
<span data-ttu-id="36e0e-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e0e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e0e-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36e0e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e0e-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36e0e-152">INPUTS</span></span>

### <span data-ttu-id="36e0e-153">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="36e0e-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="36e0e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36e0e-154">OUTPUTS</span></span>

### <span data-ttu-id="36e0e-155">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="36e0e-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="36e0e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36e0e-156">NOTES</span></span>

<span data-ttu-id="36e0e-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36e0e-157">ALIASES</span></span>

<span data-ttu-id="36e0e-158">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="36e0e-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36e0e-159">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="36e0e-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36e0e-160">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36e0e-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36e0e-161">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="36e0e-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36e0e-162">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="36e0e-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="36e0e-163">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="36e0e-164">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="36e0e-165">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="36e0e-166">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="36e0e-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36e0e-167">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36e0e-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36e0e-168">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="36e0e-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="36e0e-169">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="36e0e-170">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="36e0e-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="36e0e-171">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="36e0e-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="36e0e-172">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="36e0e-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="36e0e-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36e0e-173">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116841"
---
# <span data-ttu-id="dd5fb-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="dd5fb-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="dd5fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5fb-103">Remover um pool de host.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-103">Remove a host pool.</span></span>

## <span data-ttu-id="dd5fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd5fb-104">SYNTAX</span></span>

### <span data-ttu-id="dd5fb-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dd5fb-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd5fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5fb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd5fb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd5fb-107">DESCRIPTION</span></span>
<span data-ttu-id="dd5fb-108">Remover um pool de host.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-108">Remove a host pool.</span></span>

## <span data-ttu-id="dd5fb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd5fb-109">EXAMPLES</span></span>

### <span data-ttu-id="dd5fb-110">Exemplo 1: Excluir um HostPool da Área de Trabalho Virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="dd5fb-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="dd5fb-111">Esse comando exclui um HostPool da Área de Trabalho Virtual do Windows em um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="dd5fb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd5fb-112">PARAMETERS</span></span>

### <span data-ttu-id="dd5fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5fb-113">-DefaultProfile</span></span>
<span data-ttu-id="dd5fb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5fb-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="dd5fb-115">-Force</span></span>
<span data-ttu-id="dd5fb-116">Forçar o sinalizador a excluir sessionHost.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="dd5fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5fb-117">-InputObject</span></span>
<span data-ttu-id="dd5fb-118">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd5fb-119">-Name</span></span>
<span data-ttu-id="dd5fb-120">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd5fb-121">-PassThru</span></span>
<span data-ttu-id="dd5fb-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="dd5fb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dd5fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd5fb-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-124">The name of the resource group.</span></span>
<span data-ttu-id="dd5fb-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd5fb-126">-SubscriptionId</span></span>
<span data-ttu-id="dd5fb-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5fb-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dd5fb-128">-Confirm</span></span>
<span data-ttu-id="dd5fb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5fb-130">-WhatIf</span></span>
<span data-ttu-id="dd5fb-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5fb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5fb-133">CommonParameters</span></span>
<span data-ttu-id="dd5fb-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5fb-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd5fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5fb-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="dd5fb-136">INPUTS</span></span>

### <span data-ttu-id="dd5fb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5fb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dd5fb-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="dd5fb-138">OUTPUTS</span></span>

### <span data-ttu-id="dd5fb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd5fb-139">System.Boolean</span></span>

## <span data-ttu-id="dd5fb-140">Notas</span><span class="sxs-lookup"><span data-stu-id="dd5fb-140">NOTES</span></span>

<span data-ttu-id="dd5fb-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="dd5fb-141">ALIASES</span></span>

<span data-ttu-id="dd5fb-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="dd5fb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd5fb-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd5fb-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd5fb-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="dd5fb-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd5fb-146">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dd5fb-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dd5fb-147">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dd5fb-148">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dd5fb-149">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dd5fb-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="dd5fb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd5fb-151">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dd5fb-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dd5fb-153">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="dd5fb-154">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dd5fb-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="dd5fb-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dd5fb-156">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="dd5fb-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dd5fb-157">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="dd5fb-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dd5fb-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd5fb-158">RELATED LINKS</span></span>


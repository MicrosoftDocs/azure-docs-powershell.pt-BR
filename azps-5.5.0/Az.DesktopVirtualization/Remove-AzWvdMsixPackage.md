---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111908"
---
# <span data-ttu-id="3fa36-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3fa36-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="3fa36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fa36-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa36-103">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="3fa36-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="3fa36-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa36-104">SYNTAX</span></span>

### <span data-ttu-id="3fa36-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3fa36-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3fa36-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3fa36-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fa36-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa36-107">DESCRIPTION</span></span>
<span data-ttu-id="3fa36-108">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="3fa36-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="3fa36-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3fa36-109">EXAMPLES</span></span>

### <span data-ttu-id="3fa36-110">Exemplo 1: Excluir pacote MSIX por Nome Completo do Pacote</span><span class="sxs-lookup"><span data-stu-id="3fa36-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="3fa36-111">Este comando exclui um Pacote MSIX em um HostPool</span><span class="sxs-lookup"><span data-stu-id="3fa36-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="3fa36-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fa36-112">PARAMETERS</span></span>

### <span data-ttu-id="3fa36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa36-113">-DefaultProfile</span></span>
<span data-ttu-id="3fa36-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa36-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="3fa36-115">-FullName</span></span>
<span data-ttu-id="3fa36-116">O nome completo do pacote de versão específico do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa36-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3fa36-117">-HostPoolName</span></span>
<span data-ttu-id="3fa36-118">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3fa36-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa36-119">-InputObject</span></span>
<span data-ttu-id="3fa36-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="3fa36-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3fa36-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa36-121">-PassThru</span></span>
<span data-ttu-id="3fa36-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3fa36-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3fa36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa36-123">-ResourceGroupName</span></span>
<span data-ttu-id="3fa36-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3fa36-124">The name of the resource group.</span></span>
<span data-ttu-id="3fa36-125">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3fa36-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3fa36-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fa36-126">-SubscriptionId</span></span>
<span data-ttu-id="3fa36-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3fa36-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3fa36-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3fa36-128">-Confirm</span></span>
<span data-ttu-id="3fa36-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fa36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa36-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa36-130">-WhatIf</span></span>
<span data-ttu-id="3fa36-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3fa36-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa36-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fa36-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa36-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa36-133">CommonParameters</span></span>
<span data-ttu-id="3fa36-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa36-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa36-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fa36-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa36-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3fa36-136">INPUTS</span></span>

### <span data-ttu-id="3fa36-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3fa36-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3fa36-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="3fa36-138">OUTPUTS</span></span>

### <span data-ttu-id="3fa36-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fa36-139">System.Boolean</span></span>

## <span data-ttu-id="3fa36-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3fa36-140">NOTES</span></span>

<span data-ttu-id="3fa36-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="3fa36-141">ALIASES</span></span>

<span data-ttu-id="3fa36-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="3fa36-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3fa36-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3fa36-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3fa36-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3fa36-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3fa36-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="3fa36-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3fa36-146">`[ApplicationGroupName <String>]`: o nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3fa36-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3fa36-147">`[ApplicationName <String>]`: o nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3fa36-148">`[DesktopName <String>]`: o nome da área de trabalho dentro do grupo de área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3fa36-149">`[HostPoolName <String>]`: o nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3fa36-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3fa36-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3fa36-151">`[MsixPackageFullName <String>]`: O nome completo do pacote MSIX específico da versão dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3fa36-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3fa36-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3fa36-153">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3fa36-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="3fa36-154">`[SessionHostName <String>]`: o nome do host da sessão dentro do pool de host especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3fa36-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3fa36-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3fa36-156">`[UserSessionId <String>]`: O nome da sessão do usuário dentro do host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="3fa36-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3fa36-157">`[WorkspaceName <String>]`: o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3fa36-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3fa36-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fa36-158">RELATED LINKS</span></span>


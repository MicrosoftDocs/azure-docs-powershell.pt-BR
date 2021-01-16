---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259123"
---
# <span data-ttu-id="aefe4-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="aefe4-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="aefe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aefe4-102">SYNOPSIS</span></span>
<span data-ttu-id="aefe4-103">Remover um FileApp.</span><span class="sxs-lookup"><span data-stu-id="aefe4-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="aefe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aefe4-104">SYNTAX</span></span>

### <span data-ttu-id="aefe4-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="aefe4-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aefe4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aefe4-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aefe4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aefe4-107">DESCRIPTION</span></span>
<span data-ttu-id="aefe4-108">Remover um FileApp.</span><span class="sxs-lookup"><span data-stu-id="aefe4-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="aefe4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aefe4-109">EXAMPLES</span></span>

### <span data-ttu-id="aefe4-110">Exemplo 1: excluir um nome de aplicativo da área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="aefe4-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="aefe4-111">Este comando exclui um grupo de aplicativos de área de trabalho virtual do Windows em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aefe4-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="aefe4-112">OS</span><span class="sxs-lookup"><span data-stu-id="aefe4-112">PARAMETERS</span></span>

### <span data-ttu-id="aefe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefe4-113">-DefaultProfile</span></span>
<span data-ttu-id="aefe4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aefe4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aefe4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aefe4-115">-InputObject</span></span>
<span data-ttu-id="aefe4-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aefe4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aefe4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="aefe4-117">-Name</span></span>
<span data-ttu-id="aefe4-118">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="aefe4-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefe4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aefe4-119">-PassThru</span></span>
<span data-ttu-id="aefe4-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="aefe4-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aefe4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefe4-121">-ResourceGroupName</span></span>
<span data-ttu-id="aefe4-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aefe4-122">The name of the resource group.</span></span>
<span data-ttu-id="aefe4-123">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aefe4-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aefe4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aefe4-124">-SubscriptionId</span></span>
<span data-ttu-id="aefe4-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="aefe4-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aefe4-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aefe4-126">-Confirm</span></span>
<span data-ttu-id="aefe4-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aefe4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefe4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefe4-128">-WhatIf</span></span>
<span data-ttu-id="aefe4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aefe4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aefe4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aefe4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefe4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefe4-131">CommonParameters</span></span>
<span data-ttu-id="aefe4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefe4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefe4-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aefe4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefe4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aefe4-134">INPUTS</span></span>

### <span data-ttu-id="aefe4-135">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="aefe4-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="aefe4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aefe4-136">OUTPUTS</span></span>

### <span data-ttu-id="aefe4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aefe4-137">System.Boolean</span></span>

## <span data-ttu-id="aefe4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aefe4-138">NOTES</span></span>

<span data-ttu-id="aefe4-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aefe4-139">ALIASES</span></span>

<span data-ttu-id="aefe4-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="aefe4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aefe4-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aefe4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aefe4-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aefe4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aefe4-143">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="aefe4-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aefe4-144">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="aefe4-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="aefe4-145">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="aefe4-146">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="aefe4-147">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="aefe4-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="aefe4-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aefe4-149">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="aefe4-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aefe4-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aefe4-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="aefe4-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="aefe4-152">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="aefe4-153">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="aefe4-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aefe4-154">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="aefe4-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="aefe4-155">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="aefe4-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="aefe4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aefe4-156">RELATED LINKS</span></span>


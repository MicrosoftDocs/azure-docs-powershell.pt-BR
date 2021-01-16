---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259121"
---
# <span data-ttu-id="b054f-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="b054f-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="b054f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b054f-102">SYNOPSIS</span></span>
<span data-ttu-id="b054f-103">Remover um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b054f-103">Remove an application.</span></span>

## <span data-ttu-id="b054f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b054f-104">SYNTAX</span></span>

### <span data-ttu-id="b054f-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="b054f-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b054f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b054f-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b054f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b054f-107">DESCRIPTION</span></span>
<span data-ttu-id="b054f-108">Remover um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b054f-108">Remove an application.</span></span>

## <span data-ttu-id="b054f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b054f-109">EXAMPLES</span></span>

### <span data-ttu-id="b054f-110">Exemplo 1: excluir um aplicativo de área de trabalho virtual do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="b054f-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="b054f-111">Esse comando exclui um aplicativo de área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="b054f-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="b054f-112">OS</span><span class="sxs-lookup"><span data-stu-id="b054f-112">PARAMETERS</span></span>

### <span data-ttu-id="b054f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b054f-113">-DefaultProfile</span></span>
<span data-ttu-id="b054f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b054f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b054f-115">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="b054f-115">-GroupName</span></span>
<span data-ttu-id="b054f-116">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b054f-116">The name of the application group</span></span>

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

### <span data-ttu-id="b054f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b054f-117">-InputObject</span></span>
<span data-ttu-id="b054f-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b054f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b054f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b054f-119">-Name</span></span>
<span data-ttu-id="b054f-120">O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b054f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b054f-121">-PassThru</span></span>
<span data-ttu-id="b054f-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b054f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b054f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b054f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b054f-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b054f-124">The name of the resource group.</span></span>
<span data-ttu-id="b054f-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b054f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b054f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b054f-126">-SubscriptionId</span></span>
<span data-ttu-id="b054f-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b054f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b054f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b054f-128">-Confirm</span></span>
<span data-ttu-id="b054f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b054f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b054f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b054f-130">-WhatIf</span></span>
<span data-ttu-id="b054f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b054f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b054f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b054f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b054f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b054f-133">CommonParameters</span></span>
<span data-ttu-id="b054f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b054f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b054f-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b054f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b054f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b054f-136">INPUTS</span></span>

### <span data-ttu-id="b054f-137">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b054f-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b054f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b054f-138">OUTPUTS</span></span>

### <span data-ttu-id="b054f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b054f-139">System.Boolean</span></span>

## <span data-ttu-id="b054f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b054f-140">NOTES</span></span>

<span data-ttu-id="b054f-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b054f-141">ALIASES</span></span>

<span data-ttu-id="b054f-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b054f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b054f-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b054f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b054f-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b054f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b054f-145">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b054f-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b054f-146">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b054f-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b054f-147">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b054f-148">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b054f-149">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b054f-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b054f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b054f-151">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b054f-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b054f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b054f-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b054f-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b054f-154">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b054f-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b054f-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b054f-156">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="b054f-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b054f-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="b054f-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b054f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b054f-158">RELATED LINKS</span></span>


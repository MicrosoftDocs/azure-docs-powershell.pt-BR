---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257551"
---
# <span data-ttu-id="fb8b5-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fb8b5-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="fb8b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8b5-103">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="fb8b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb8b5-104">SYNTAX</span></span>

### <span data-ttu-id="fb8b5-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb8b5-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb8b5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb8b5-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb8b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb8b5-107">DESCRIPTION</span></span>
<span data-ttu-id="fb8b5-108">Remover um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="fb8b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb8b5-109">EXAMPLES</span></span>

### <span data-ttu-id="fb8b5-110">Exemplo 1: excluir pacote MSIX por nome completo do pacote</span><span class="sxs-lookup"><span data-stu-id="fb8b5-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="fb8b5-111">Esse comando exclui um pacote MSIX em um HostPool</span><span class="sxs-lookup"><span data-stu-id="fb8b5-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="fb8b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb8b5-112">PARAMETERS</span></span>

### <span data-ttu-id="fb8b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8b5-113">-DefaultProfile</span></span>
<span data-ttu-id="fb8b5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb8b5-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="fb8b5-115">-FullName</span></span>
<span data-ttu-id="fb8b5-116">O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="fb8b5-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="fb8b5-117">-HostPoolName</span></span>
<span data-ttu-id="fb8b5-118">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="fb8b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb8b5-119">-InputObject</span></span>
<span data-ttu-id="fb8b5-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb8b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb8b5-121">-PassThru</span></span>
<span data-ttu-id="fb8b5-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fb8b5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb8b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb8b5-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-124">The name of the resource group.</span></span>
<span data-ttu-id="fb8b5-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb8b5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb8b5-126">-SubscriptionId</span></span>
<span data-ttu-id="fb8b5-127">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb8b5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb8b5-128">-Confirm</span></span>
<span data-ttu-id="fb8b5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8b5-130">-WhatIf</span></span>
<span data-ttu-id="fb8b5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8b5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb8b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8b5-133">CommonParameters</span></span>
<span data-ttu-id="fb8b5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8b5-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb8b5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8b5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb8b5-136">INPUTS</span></span>

### <span data-ttu-id="fb8b5-137">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="fb8b5-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fb8b5-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb8b5-138">OUTPUTS</span></span>

### <span data-ttu-id="fb8b5-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb8b5-139">System.Boolean</span></span>

## <span data-ttu-id="fb8b5-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb8b5-140">NOTES</span></span>

<span data-ttu-id="fb8b5-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb8b5-141">ALIASES</span></span>

<span data-ttu-id="fb8b5-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fb8b5-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb8b5-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb8b5-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb8b5-145">INPUTobject <IDesktopVirtualizationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fb8b5-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb8b5-146">`[ApplicationGroupName <String>]`: O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="fb8b5-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fb8b5-147">`[ApplicationName <String>]`: O nome do aplicativo dentro do grupo de aplicativos especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fb8b5-148">`[DesktopName <String>]`: O nome da área de trabalho dentro do grupo da área de trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fb8b5-149">`[HostPoolName <String>]`: O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fb8b5-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fb8b5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb8b5-151">`[MsixPackageFullName <String>]`: O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="fb8b5-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb8b5-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb8b5-154">`[SessionHostName <String>]`: O nome do host da sessão dentro do pool de hosts especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fb8b5-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fb8b5-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fb8b5-156">`[UserSessionId <String>]`: O nome da sessão do usuário no host de sessão especificado</span><span class="sxs-lookup"><span data-stu-id="fb8b5-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fb8b5-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="fb8b5-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fb8b5-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb8b5-158">RELATED LINKS</span></span>


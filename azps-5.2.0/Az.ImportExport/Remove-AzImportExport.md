---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263267"
---
# <span data-ttu-id="52e04-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="52e04-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="52e04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52e04-102">SYNOPSIS</span></span>
<span data-ttu-id="52e04-103">Exclui um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="52e04-103">Deletes an existing job.</span></span>
<span data-ttu-id="52e04-104">Somente os trabalhos nos Estados criando ou concluídos podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="52e04-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="52e04-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52e04-105">SYNTAX</span></span>

### <span data-ttu-id="52e04-106">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="52e04-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52e04-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52e04-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52e04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52e04-108">DESCRIPTION</span></span>
<span data-ttu-id="52e04-109">Exclui um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="52e04-109">Deletes an existing job.</span></span>
<span data-ttu-id="52e04-110">Somente os trabalhos nos Estados criando ou concluídos podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="52e04-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="52e04-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52e04-111">EXAMPLES</span></span>

### <span data-ttu-id="52e04-112">Exemplo 1: remover o trabalho do ImportExport por meio da Resource e do nome do servidor</span><span class="sxs-lookup"><span data-stu-id="52e04-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="52e04-113">Esse cmdlet Remove o trabalho do ImportExport por meio da Resource e do nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="52e04-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="52e04-114">Exemplo 2: remover o trabalho ImportExport por identidade</span><span class="sxs-lookup"><span data-stu-id="52e04-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="52e04-115">Esse cmdlet Remove o trabalho ImportExport por identidade.</span><span class="sxs-lookup"><span data-stu-id="52e04-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="52e04-116">OS</span><span class="sxs-lookup"><span data-stu-id="52e04-116">PARAMETERS</span></span>

### <span data-ttu-id="52e04-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="52e04-117">-AcceptLanguage</span></span>
<span data-ttu-id="52e04-118">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="52e04-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="52e04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e04-119">-DefaultProfile</span></span>
<span data-ttu-id="52e04-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52e04-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52e04-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52e04-121">-InputObject</span></span>
<span data-ttu-id="52e04-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52e04-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52e04-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="52e04-123">-Name</span></span>
<span data-ttu-id="52e04-124">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="52e04-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e04-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52e04-125">-PassThru</span></span>
<span data-ttu-id="52e04-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="52e04-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52e04-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e04-127">-ResourceGroupName</span></span>
<span data-ttu-id="52e04-128">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="52e04-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="52e04-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52e04-129">-SubscriptionId</span></span>
<span data-ttu-id="52e04-130">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="52e04-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="52e04-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52e04-131">-Confirm</span></span>
<span data-ttu-id="52e04-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52e04-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e04-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e04-133">-WhatIf</span></span>
<span data-ttu-id="52e04-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52e04-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52e04-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52e04-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e04-136">CommonParameters</span></span>
<span data-ttu-id="52e04-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e04-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52e04-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e04-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52e04-139">INPUTS</span></span>

### <span data-ttu-id="52e04-140">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="52e04-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="52e04-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52e04-141">OUTPUTS</span></span>

### <span data-ttu-id="52e04-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52e04-142">System.Boolean</span></span>

## <span data-ttu-id="52e04-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52e04-143">NOTES</span></span>

<span data-ttu-id="52e04-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52e04-144">ALIASES</span></span>

<span data-ttu-id="52e04-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="52e04-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52e04-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="52e04-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52e04-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52e04-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52e04-148">INPUTobject <IImportExportIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="52e04-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52e04-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="52e04-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52e04-150">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="52e04-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="52e04-151">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="52e04-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="52e04-152">Por exemplo, Oeste EUA ou oesteus.</span><span class="sxs-lookup"><span data-stu-id="52e04-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="52e04-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="52e04-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="52e04-154">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="52e04-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="52e04-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52e04-155">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776008"
---
# <span data-ttu-id="e2ece-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="e2ece-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="e2ece-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2ece-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ece-103">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="e2ece-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e2ece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2ece-104">SYNTAX</span></span>

### <span data-ttu-id="e2ece-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2ece-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2ece-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ece-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2ece-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2ece-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ece-108">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="e2ece-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e2ece-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2ece-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ece-110">Exemplo 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="e2ece-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="e2ece-111">Exclui TestUbuntu. Test. 1.0.0 da Galeria de pilhas do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ece-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="e2ece-112">Exemplo 2: Remove-AzsGalleryItem por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="e2ece-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="e2ece-113">Exclui TestUbuntu. Test. 1.0.0 pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e2ece-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="e2ece-114">OS</span><span class="sxs-lookup"><span data-stu-id="e2ece-114">PARAMETERS</span></span>

### <span data-ttu-id="e2ece-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ece-115">-DefaultProfile</span></span>
<span data-ttu-id="e2ece-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ece-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ece-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ece-117">-InputObject</span></span>
<span data-ttu-id="e2ece-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e2ece-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e2ece-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2ece-119">-Name</span></span>
<span data-ttu-id="e2ece-120">Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="e2ece-120">Identity of the gallery item.</span></span>
<span data-ttu-id="e2ece-121">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="e2ece-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2ece-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2ece-122">-PassThru</span></span>
<span data-ttu-id="e2ece-123">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e2ece-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2ece-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2ece-124">-SubscriptionId</span></span>
<span data-ttu-id="e2ece-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ece-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2ece-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ece-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2ece-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2ece-127">-Confirm</span></span>
<span data-ttu-id="e2ece-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ece-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ece-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ece-129">-WhatIf</span></span>
<span data-ttu-id="e2ece-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2ece-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ece-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2ece-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ece-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ece-132">CommonParameters</span></span>
<span data-ttu-id="e2ece-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ece-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ece-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2ece-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ece-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2ece-135">INPUTS</span></span>

### <span data-ttu-id="e2ece-136">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ece-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="e2ece-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2ece-137">OUTPUTS</span></span>

### <span data-ttu-id="e2ece-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2ece-138">System.Boolean</span></span>



## <span data-ttu-id="e2ece-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2ece-139">NOTES</span></span>

<span data-ttu-id="e2ece-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e2ece-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2ece-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2ece-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e2ece-142">INPUTobject <IGalleryIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e2ece-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2ece-143">`[GalleryItemName <String>]`: Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="e2ece-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="e2ece-144">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="e2ece-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="e2ece-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e2ece-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2ece-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ece-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2ece-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e2ece-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e2ece-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2ece-148">RELATED LINKS</span></span>


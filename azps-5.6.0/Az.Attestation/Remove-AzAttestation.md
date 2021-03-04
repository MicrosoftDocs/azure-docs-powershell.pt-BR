---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887038"
---
# <span data-ttu-id="9821d-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="9821d-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="9821d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9821d-102">SYNOPSIS</span></span>
<span data-ttu-id="9821d-103">Exclui um atestado.</span><span class="sxs-lookup"><span data-stu-id="9821d-103">Deletes an attestation.</span></span>

## <span data-ttu-id="9821d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9821d-104">SYNTAX</span></span>

### <span data-ttu-id="9821d-105">ByAvailableAttestation (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9821d-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9821d-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="9821d-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9821d-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="9821d-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9821d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9821d-108">DESCRIPTION</span></span>
<span data-ttu-id="9821d-109">O Remove-AzAttestation cmdlet exclui o atestado especificado.</span><span class="sxs-lookup"><span data-stu-id="9821d-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="9821d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9821d-110">EXAMPLES</span></span>

### <span data-ttu-id="9821d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9821d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="9821d-112">Exclua o Provedor de Atestado chamado *pshtest3* no grupo de recursos chamado *psh-test-rg* da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9821d-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="9821d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9821d-113">PARAMETERS</span></span>

### <span data-ttu-id="9821d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9821d-114">-DefaultProfile</span></span>
<span data-ttu-id="9821d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9821d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9821d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9821d-116">-InputObject</span></span>
<span data-ttu-id="9821d-117">Objeto de atestado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9821d-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9821d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9821d-118">-Name</span></span>
<span data-ttu-id="9821d-119">Especifica o nome do atestado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9821d-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9821d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9821d-120">-PassThru</span></span>
<span data-ttu-id="9821d-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="9821d-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9821d-122">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="9821d-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9821d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9821d-123">-ResourceGroupName</span></span>
<span data-ttu-id="9821d-124">Especifica o nome do grupo de recursos para o atestado do Azure ser removido.</span><span class="sxs-lookup"><span data-stu-id="9821d-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9821d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9821d-125">-ResourceId</span></span>
<span data-ttu-id="9821d-126">ID do Recurso de Atestado.</span><span class="sxs-lookup"><span data-stu-id="9821d-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9821d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9821d-127">-Confirm</span></span>
<span data-ttu-id="9821d-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9821d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9821d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9821d-129">-WhatIf</span></span>
<span data-ttu-id="9821d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9821d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9821d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9821d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9821d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9821d-132">CommonParameters</span></span>
<span data-ttu-id="9821d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9821d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9821d-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9821d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9821d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9821d-135">INPUTS</span></span>

### <span data-ttu-id="9821d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9821d-136">System.String</span></span>

### <span data-ttu-id="9821d-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="9821d-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="9821d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9821d-138">OUTPUTS</span></span>

### <span data-ttu-id="9821d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9821d-139">System.Boolean</span></span>

## <span data-ttu-id="9821d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="9821d-140">NOTES</span></span>

## <span data-ttu-id="9821d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9821d-141">RELATED LINKS</span></span>

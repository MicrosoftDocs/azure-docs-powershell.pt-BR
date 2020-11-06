---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597882"
---
# <span data-ttu-id="3c135-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="3c135-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="3c135-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c135-102">SYNOPSIS</span></span>
<span data-ttu-id="3c135-103">Exclui um atestado.</span><span class="sxs-lookup"><span data-stu-id="3c135-103">Deletes an attestation.</span></span>

## <span data-ttu-id="3c135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c135-104">SYNTAX</span></span>

### <span data-ttu-id="3c135-105">ByAvailableAttestation (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c135-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c135-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="3c135-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c135-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="3c135-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c135-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c135-108">DESCRIPTION</span></span>
<span data-ttu-id="3c135-109">O cmdlet Remove-AzAttestation exclui o atestado especificado.</span><span class="sxs-lookup"><span data-stu-id="3c135-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="3c135-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c135-110">EXAMPLES</span></span>

### <span data-ttu-id="3c135-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c135-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="3c135-112">Excluir atestado "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="3c135-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="3c135-113">OS</span><span class="sxs-lookup"><span data-stu-id="3c135-113">PARAMETERS</span></span>

### <span data-ttu-id="3c135-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c135-114">-AsJob</span></span>
<span data-ttu-id="3c135-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c135-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c135-116">-DefaultProfile</span></span>
<span data-ttu-id="3c135-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c135-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c135-118">-InputObject</span></span>
<span data-ttu-id="3c135-119">Objeto de atestado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3c135-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c135-120">-Name</span></span>
<span data-ttu-id="3c135-121">Especifica o nome do atestado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3c135-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c135-122">-PassThru</span></span>
<span data-ttu-id="3c135-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="3c135-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3c135-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3c135-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c135-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c135-126">Especifica o nome do grupo de recursos para o atestado do Azure remover.</span><span class="sxs-lookup"><span data-stu-id="3c135-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c135-127">-ResourceId</span></span>
<span data-ttu-id="3c135-128">ID do recurso de atestado.</span><span class="sxs-lookup"><span data-stu-id="3c135-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c135-129">-Confirm</span></span>
<span data-ttu-id="3c135-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c135-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c135-131">-WhatIf</span></span>
<span data-ttu-id="3c135-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c135-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c135-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c135-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c135-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c135-134">CommonParameters</span></span>
<span data-ttu-id="3c135-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c135-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c135-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c135-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c135-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c135-137">INPUTS</span></span>

### <span data-ttu-id="3c135-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3c135-138">System.String</span></span>

### <span data-ttu-id="3c135-139">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="3c135-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="3c135-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c135-140">OUTPUTS</span></span>

### <span data-ttu-id="3c135-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c135-141">System.Boolean</span></span>

## <span data-ttu-id="3c135-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c135-142">NOTES</span></span>

## <span data-ttu-id="3c135-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c135-143">RELATED LINKS</span></span>

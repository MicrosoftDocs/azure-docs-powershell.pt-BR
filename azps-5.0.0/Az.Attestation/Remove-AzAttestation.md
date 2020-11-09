---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281497"
---
# <span data-ttu-id="6097f-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="6097f-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="6097f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6097f-102">SYNOPSIS</span></span>
<span data-ttu-id="6097f-103">Exclui um atestado.</span><span class="sxs-lookup"><span data-stu-id="6097f-103">Deletes an attestation.</span></span>

## <span data-ttu-id="6097f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6097f-104">SYNTAX</span></span>

### <span data-ttu-id="6097f-105">ByAvailableAttestation (padrão)</span><span class="sxs-lookup"><span data-stu-id="6097f-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6097f-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="6097f-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6097f-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="6097f-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6097f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6097f-108">DESCRIPTION</span></span>
<span data-ttu-id="6097f-109">O cmdlet Remove-AzAttestation exclui o atestado especificado.</span><span class="sxs-lookup"><span data-stu-id="6097f-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="6097f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6097f-110">EXAMPLES</span></span>

### <span data-ttu-id="6097f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6097f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="6097f-112">Exclua o provedor de atestado chamado *pshtest3* no grupo de recursos chamado *PSH-Test-RG* da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6097f-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="6097f-113">OS</span><span class="sxs-lookup"><span data-stu-id="6097f-113">PARAMETERS</span></span>

### <span data-ttu-id="6097f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6097f-114">-DefaultProfile</span></span>
<span data-ttu-id="6097f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6097f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6097f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6097f-116">-InputObject</span></span>
<span data-ttu-id="6097f-117">Objeto de atestado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6097f-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="6097f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6097f-118">-Name</span></span>
<span data-ttu-id="6097f-119">Especifica o nome do atestado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6097f-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="6097f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6097f-120">-PassThru</span></span>
<span data-ttu-id="6097f-121">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="6097f-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6097f-122">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6097f-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6097f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6097f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6097f-124">Especifica o nome do grupo de recursos para o atestado do Azure remover.</span><span class="sxs-lookup"><span data-stu-id="6097f-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="6097f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6097f-125">-ResourceId</span></span>
<span data-ttu-id="6097f-126">ID do recurso de atestado.</span><span class="sxs-lookup"><span data-stu-id="6097f-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="6097f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6097f-127">-Confirm</span></span>
<span data-ttu-id="6097f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6097f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6097f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6097f-129">-WhatIf</span></span>
<span data-ttu-id="6097f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6097f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6097f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6097f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6097f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6097f-132">CommonParameters</span></span>
<span data-ttu-id="6097f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6097f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6097f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6097f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6097f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6097f-135">INPUTS</span></span>

### <span data-ttu-id="6097f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6097f-136">System.String</span></span>

### <span data-ttu-id="6097f-137">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="6097f-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="6097f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6097f-138">OUTPUTS</span></span>

### <span data-ttu-id="6097f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6097f-139">System.Boolean</span></span>

## <span data-ttu-id="6097f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6097f-140">NOTES</span></span>

## <span data-ttu-id="6097f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6097f-141">RELATED LINKS</span></span>

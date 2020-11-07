---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956033"
---
# <span data-ttu-id="09832-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="09832-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="09832-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09832-102">SYNOPSIS</span></span>
<span data-ttu-id="09832-103">Exclui um atestado.</span><span class="sxs-lookup"><span data-stu-id="09832-103">Deletes an attestation.</span></span>

## <span data-ttu-id="09832-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09832-104">SYNTAX</span></span>

### <span data-ttu-id="09832-105">ByAvailableAttestation (padrão)</span><span class="sxs-lookup"><span data-stu-id="09832-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09832-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="09832-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09832-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="09832-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09832-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09832-108">DESCRIPTION</span></span>
<span data-ttu-id="09832-109">O cmdlet Remove-AzAttestation exclui o atestado especificado.</span><span class="sxs-lookup"><span data-stu-id="09832-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="09832-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09832-110">EXAMPLES</span></span>

### <span data-ttu-id="09832-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09832-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="09832-112">Exclua o provedor de atestado chamado *pshtest3* no grupo de recursos chamado *PSH-Test-RG* da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="09832-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="09832-113">OS</span><span class="sxs-lookup"><span data-stu-id="09832-113">PARAMETERS</span></span>

### <span data-ttu-id="09832-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09832-114">-DefaultProfile</span></span>
<span data-ttu-id="09832-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09832-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09832-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09832-116">-InputObject</span></span>
<span data-ttu-id="09832-117">Objeto de atestado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="09832-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="09832-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="09832-118">-Name</span></span>
<span data-ttu-id="09832-119">Especifica o nome do atestado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="09832-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="09832-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09832-120">-PassThru</span></span>
<span data-ttu-id="09832-121">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="09832-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="09832-122">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="09832-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="09832-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09832-123">-ResourceGroupName</span></span>
<span data-ttu-id="09832-124">Especifica o nome do grupo de recursos para o atestado do Azure remover.</span><span class="sxs-lookup"><span data-stu-id="09832-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="09832-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09832-125">-ResourceId</span></span>
<span data-ttu-id="09832-126">ID do recurso de atestado.</span><span class="sxs-lookup"><span data-stu-id="09832-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="09832-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09832-127">-Confirm</span></span>
<span data-ttu-id="09832-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09832-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09832-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09832-129">-WhatIf</span></span>
<span data-ttu-id="09832-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09832-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09832-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09832-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09832-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09832-132">CommonParameters</span></span>
<span data-ttu-id="09832-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09832-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09832-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09832-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09832-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09832-135">INPUTS</span></span>

### <span data-ttu-id="09832-136">System. String</span><span class="sxs-lookup"><span data-stu-id="09832-136">System.String</span></span>

### <span data-ttu-id="09832-137">Microsoft. Azure. Commands.. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="09832-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="09832-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09832-138">OUTPUTS</span></span>

### <span data-ttu-id="09832-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09832-139">System.Boolean</span></span>

## <span data-ttu-id="09832-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09832-140">NOTES</span></span>

## <span data-ttu-id="09832-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09832-141">RELATED LINKS</span></span>

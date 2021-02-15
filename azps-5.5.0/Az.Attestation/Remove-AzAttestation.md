---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112271"
---
# <span data-ttu-id="deb2b-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="deb2b-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="deb2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="deb2b-103">Exclui um teste.</span><span class="sxs-lookup"><span data-stu-id="deb2b-103">Deletes an attestation.</span></span>

## <span data-ttu-id="deb2b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deb2b-104">SYNTAX</span></span>

### <span data-ttu-id="deb2b-105">Estação ByAvailableAtte (Padrão)</span><span class="sxs-lookup"><span data-stu-id="deb2b-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb2b-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="deb2b-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb2b-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="deb2b-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb2b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="deb2b-108">DESCRIPTION</span></span>
<span data-ttu-id="deb2b-109">O Remove-AzAttestation cmdlet exclui o teste especificado.</span><span class="sxs-lookup"><span data-stu-id="deb2b-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="deb2b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="deb2b-110">EXAMPLES</span></span>

### <span data-ttu-id="deb2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deb2b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="deb2b-112">Exclua o Provedor de Teste chamado *pshtest3* no grupo de recursos chamado *psh-test-rg* da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="deb2b-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="deb2b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deb2b-113">PARAMETERS</span></span>

### <span data-ttu-id="deb2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb2b-114">-DefaultProfile</span></span>
<span data-ttu-id="deb2b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deb2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb2b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deb2b-116">-InputObject</span></span>
<span data-ttu-id="deb2b-117">Objeto de teste a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="deb2b-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="deb2b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="deb2b-118">-Name</span></span>
<span data-ttu-id="deb2b-119">Especifica o nome do teste a ser removido.</span><span class="sxs-lookup"><span data-stu-id="deb2b-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="deb2b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="deb2b-120">-PassThru</span></span>
<span data-ttu-id="deb2b-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="deb2b-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="deb2b-122">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="deb2b-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="deb2b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb2b-123">-ResourceGroupName</span></span>
<span data-ttu-id="deb2b-124">Especifica o nome do grupo de recursos a ser removido do Azure.</span><span class="sxs-lookup"><span data-stu-id="deb2b-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="deb2b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deb2b-125">-ResourceId</span></span>
<span data-ttu-id="deb2b-126">ID do Recurso de Teste.</span><span class="sxs-lookup"><span data-stu-id="deb2b-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="deb2b-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="deb2b-127">-Confirm</span></span>
<span data-ttu-id="deb2b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb2b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb2b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb2b-129">-WhatIf</span></span>
<span data-ttu-id="deb2b-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="deb2b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb2b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deb2b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb2b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb2b-132">CommonParameters</span></span>
<span data-ttu-id="deb2b-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb2b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb2b-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="deb2b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb2b-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="deb2b-135">INPUTS</span></span>

### <span data-ttu-id="deb2b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="deb2b-136">System.String</span></span>

### <span data-ttu-id="deb2b-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="deb2b-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="deb2b-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="deb2b-138">OUTPUTS</span></span>

### <span data-ttu-id="deb2b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="deb2b-139">System.Boolean</span></span>

## <span data-ttu-id="deb2b-140">Notas</span><span class="sxs-lookup"><span data-stu-id="deb2b-140">NOTES</span></span>

## <span data-ttu-id="deb2b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deb2b-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118205"
---
# <span data-ttu-id="0db11-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="0db11-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0db11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0db11-102">SYNOPSIS</span></span>
<span data-ttu-id="0db11-103">Exclua ou remova uma ASN registrada do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="0db11-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="0db11-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0db11-104">SYNTAX</span></span>

### <span data-ttu-id="0db11-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="0db11-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db11-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0db11-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db11-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0db11-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db11-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0db11-108">DESCRIPTION</span></span>
<span data-ttu-id="0db11-109">Permite a remoção do ASN registrado do recurso de parêntese pai.</span><span class="sxs-lookup"><span data-stu-id="0db11-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="0db11-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0db11-110">EXAMPLES</span></span>

### <span data-ttu-id="0db11-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0db11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="0db11-112">Remover um ASN registrado por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0db11-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="0db11-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0db11-113">PARAMETERS</span></span>

### <span data-ttu-id="0db11-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0db11-114">-AsJob</span></span>
<span data-ttu-id="0db11-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0db11-115">Run in the background.</span></span>

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

### <span data-ttu-id="0db11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db11-116">-DefaultProfile</span></span>
<span data-ttu-id="0db11-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0db11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db11-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0db11-118">-Force</span></span>
<span data-ttu-id="0db11-119">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="0db11-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="0db11-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db11-120">-InputObject</span></span>
<span data-ttu-id="0db11-121">Usar um Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="0db11-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0db11-122">-Name</span></span>
<span data-ttu-id="0db11-123">O nome da ASN registrada</span><span class="sxs-lookup"><span data-stu-id="0db11-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0db11-124">-PassThru</span></span>
<span data-ttu-id="0db11-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0db11-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0db11-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="0db11-126">-PeeringName</span></span>
<span data-ttu-id="0db11-127">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="0db11-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db11-128">-ResourceGroupName</span></span>
<span data-ttu-id="0db11-129">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="0db11-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db11-130">-ResourceId</span></span>
<span data-ttu-id="0db11-131">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0db11-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0db11-132">-Confirm</span></span>
<span data-ttu-id="0db11-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db11-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db11-134">-WhatIf</span></span>
<span data-ttu-id="0db11-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0db11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db11-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0db11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db11-137">CommonParameters</span></span>
<span data-ttu-id="0db11-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db11-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0db11-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db11-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="0db11-140">INPUTS</span></span>

### <span data-ttu-id="0db11-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="0db11-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="0db11-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0db11-142">System.String</span></span>

## <span data-ttu-id="0db11-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="0db11-143">OUTPUTS</span></span>

### <span data-ttu-id="0db11-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0db11-144">System.Boolean</span></span>

## <span data-ttu-id="0db11-145">Notas</span><span class="sxs-lookup"><span data-stu-id="0db11-145">NOTES</span></span>

## <span data-ttu-id="0db11-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0db11-146">RELATED LINKS</span></span>

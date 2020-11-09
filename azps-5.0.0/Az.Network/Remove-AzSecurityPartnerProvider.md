---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282155"
---
# <span data-ttu-id="2d44e-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d44e-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d44e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d44e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d44e-103">Exclui um SecurityPartnerProvider do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d44e-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2d44e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d44e-104">SYNTAX</span></span>

### <span data-ttu-id="2d44e-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d44e-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d44e-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d44e-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d44e-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d44e-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d44e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d44e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d44e-109">O cmdlet **Remove-AzSecurityPartnerProvider** exclui um Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d44e-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2d44e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d44e-110">EXAMPLES</span></span>

### <span data-ttu-id="2d44e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d44e-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="2d44e-112">OS</span><span class="sxs-lookup"><span data-stu-id="2d44e-112">PARAMETERS</span></span>

### <span data-ttu-id="2d44e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d44e-113">-AsJob</span></span>
<span data-ttu-id="2d44e-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d44e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d44e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d44e-115">-DefaultProfile</span></span>
<span data-ttu-id="2d44e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d44e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d44e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d44e-117">-Force</span></span>
<span data-ttu-id="2d44e-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2d44e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d44e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d44e-119">-Name</span></span>
<span data-ttu-id="2d44e-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2d44e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d44e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d44e-121">-PassThru</span></span>
<span data-ttu-id="2d44e-122">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="2d44e-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2d44e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d44e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d44e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d44e-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d44e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d44e-125">-ResourceId</span></span>
<span data-ttu-id="2d44e-126">A ID do recurso securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2d44e-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d44e-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d44e-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="2d44e-128">O objeto de entrada securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2d44e-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d44e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d44e-129">-Confirm</span></span>
<span data-ttu-id="2d44e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d44e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d44e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d44e-131">-WhatIf</span></span>
<span data-ttu-id="2d44e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d44e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d44e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d44e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d44e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d44e-134">CommonParameters</span></span>
<span data-ttu-id="2d44e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d44e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d44e-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d44e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d44e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d44e-137">INPUTS</span></span>

### <span data-ttu-id="2d44e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2d44e-138">System.String</span></span>

### <span data-ttu-id="2d44e-139">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d44e-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d44e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d44e-140">OUTPUTS</span></span>

### <span data-ttu-id="2d44e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d44e-141">System.Boolean</span></span>

## <span data-ttu-id="2d44e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d44e-142">NOTES</span></span>

## <span data-ttu-id="2d44e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d44e-143">RELATED LINKS</span></span>

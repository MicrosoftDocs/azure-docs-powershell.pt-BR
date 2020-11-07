---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786414"
---
# <span data-ttu-id="0c3d8-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c3d8-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="0c3d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3d8-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="0c3d8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c3d8-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c3d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3d8-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="0c3d8-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0c3d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c3d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3d8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c3d8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0c3d8-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="0c3d8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0c3d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="0c3d8-110">PARAMETERS</span></span>

### <span data-ttu-id="0c3d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3d8-111">-DefaultProfile</span></span>
<span data-ttu-id="0c3d8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3d8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0c3d8-113">-Force</span></span>
<span data-ttu-id="0c3d8-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0c3d8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3d8-115">-Name</span></span>
<span data-ttu-id="0c3d8-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3d8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c3d8-117">-PassThru</span></span>
<span data-ttu-id="0c3d8-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="0c3d8-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0c3d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c3d8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3d8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c3d8-121">-Confirm</span></span>
<span data-ttu-id="0c3d8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3d8-123">-WhatIf</span></span>
<span data-ttu-id="0c3d8-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3d8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3d8-126">CommonParameters</span></span>
<span data-ttu-id="0c3d8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3d8-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3d8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c3d8-129">INPUTS</span></span>

### <span data-ttu-id="0c3d8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3d8-130">System.String</span></span>

## <span data-ttu-id="0c3d8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c3d8-131">OUTPUTS</span></span>

### <span data-ttu-id="0c3d8-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="0c3d8-132">System.Object</span></span>

## <span data-ttu-id="0c3d8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c3d8-133">NOTES</span></span>

## <span data-ttu-id="0c3d8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c3d8-134">RELATED LINKS</span></span>


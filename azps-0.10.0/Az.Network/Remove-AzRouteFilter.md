---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776610"
---
# <span data-ttu-id="f0746-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f0746-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="f0746-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0746-102">SYNOPSIS</span></span>
<span data-ttu-id="f0746-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="f0746-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="f0746-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0746-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0746-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0746-105">DESCRIPTION</span></span>
<span data-ttu-id="f0746-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="f0746-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f0746-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0746-107">EXAMPLES</span></span>

### <span data-ttu-id="f0746-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0746-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f0746-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="f0746-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f0746-110">OS</span><span class="sxs-lookup"><span data-stu-id="f0746-110">PARAMETERS</span></span>

### <span data-ttu-id="f0746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0746-111">-DefaultProfile</span></span>
<span data-ttu-id="f0746-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0746-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0746-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f0746-113">-Force</span></span>
<span data-ttu-id="f0746-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f0746-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f0746-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0746-115">-Name</span></span>
<span data-ttu-id="f0746-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0746-116">The resource name.</span></span>

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

### <span data-ttu-id="f0746-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0746-117">-PassThru</span></span>
<span data-ttu-id="f0746-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f0746-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f0746-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0746-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0746-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0746-120">The resource group name.</span></span>

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

### <span data-ttu-id="f0746-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0746-121">-Confirm</span></span>
<span data-ttu-id="f0746-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0746-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0746-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0746-123">-WhatIf</span></span>
<span data-ttu-id="f0746-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0746-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0746-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0746-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0746-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0746-126">CommonParameters</span></span>
<span data-ttu-id="f0746-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0746-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0746-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0746-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0746-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0746-129">INPUTS</span></span>

### <span data-ttu-id="f0746-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f0746-130">System.String</span></span>

## <span data-ttu-id="f0746-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0746-131">OUTPUTS</span></span>

### <span data-ttu-id="f0746-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="f0746-132">System.Object</span></span>

## <span data-ttu-id="f0746-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0746-133">NOTES</span></span>

## <span data-ttu-id="f0746-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0746-134">RELATED LINKS</span></span>


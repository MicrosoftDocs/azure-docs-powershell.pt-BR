---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 3f7e0a96212e9de87c90cffd059801084da471ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430137"
---
# <span data-ttu-id="9c4e9-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c4e9-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9c4e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4e9-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="9c4e9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c4e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c4e9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c4e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c4e9-105">DESCRIPTION</span></span>
<span data-ttu-id="9c4e9-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="9c4e9-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9c4e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c4e9-107">EXAMPLES</span></span>

### <span data-ttu-id="9c4e9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c4e9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9c4e9-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="9c4e9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9c4e9-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c4e9-110">PARAMETERS</span></span>

### <span data-ttu-id="9c4e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4e9-111">-DefaultProfile</span></span>
<span data-ttu-id="9c4e9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4e9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c4e9-113">-Force</span></span>
<span data-ttu-id="9c4e9-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9c4e9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c4e9-115">-Name</span></span>
<span data-ttu-id="9c4e9-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4e9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c4e9-117">-PassThru</span></span>
<span data-ttu-id="9c4e9-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9c4e9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9c4e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c4e9-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4e9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c4e9-121">-Confirm</span></span>
<span data-ttu-id="9c4e9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c4e9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4e9-123">-WhatIf</span></span>
<span data-ttu-id="9c4e9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c4e9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c4e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4e9-126">CommonParameters</span></span>
<span data-ttu-id="9c4e9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4e9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4e9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c4e9-129">INPUTS</span></span>

### <span data-ttu-id="9c4e9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9c4e9-130">System.String</span></span>

## <span data-ttu-id="9c4e9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c4e9-131">OUTPUTS</span></span>

### <span data-ttu-id="9c4e9-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c4e9-132">System.Boolean</span></span>

## <span data-ttu-id="9c4e9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c4e9-133">NOTES</span></span>

## <span data-ttu-id="9c4e9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c4e9-134">RELATED LINKS</span></span>

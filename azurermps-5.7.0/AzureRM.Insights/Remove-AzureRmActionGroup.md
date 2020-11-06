---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432495"
---
# <span data-ttu-id="956e5-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="956e5-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="956e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="956e5-102">SYNOPSIS</span></span>
<span data-ttu-id="956e5-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="956e5-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="956e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="956e5-104">SYNTAX</span></span>

### <span data-ttu-id="956e5-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="956e5-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="956e5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="956e5-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="956e5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="956e5-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956e5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="956e5-108">DESCRIPTION</span></span>
<span data-ttu-id="956e5-109">O cmdlet **Remove-AzureRmActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="956e5-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="956e5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="956e5-110">EXAMPLES</span></span>

### <span data-ttu-id="956e5-111">Exemplo 1: remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="956e5-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="956e5-112">OS</span><span class="sxs-lookup"><span data-stu-id="956e5-112">PARAMETERS</span></span>

### <span data-ttu-id="956e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956e5-113">-DefaultProfile</span></span>
<span data-ttu-id="956e5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="956e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="956e5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="956e5-115">-InputObject</span></span>
<span data-ttu-id="956e5-116">O grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="956e5-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="956e5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="956e5-117">-Name</span></span>
<span data-ttu-id="956e5-118">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="956e5-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="956e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="956e5-120">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="956e5-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956e5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="956e5-121">-ResourceId</span></span>
<span data-ttu-id="956e5-122">O recurso i</span><span class="sxs-lookup"><span data-stu-id="956e5-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956e5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="956e5-123">-Confirm</span></span>
<span data-ttu-id="956e5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="956e5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956e5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956e5-125">-WhatIf</span></span>
<span data-ttu-id="956e5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="956e5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="956e5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="956e5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956e5-128">CommonParameters</span></span>
<span data-ttu-id="956e5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956e5-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956e5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956e5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="956e5-131">INPUTS</span></span>

### <span data-ttu-id="956e5-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="956e5-132">None</span></span>
<span data-ttu-id="956e5-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="956e5-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="956e5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="956e5-134">OUTPUTS</span></span>

### <span data-ttu-id="956e5-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="956e5-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="956e5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="956e5-136">NOTES</span></span>

## <span data-ttu-id="956e5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="956e5-137">RELATED LINKS</span></span>

<span data-ttu-id="956e5-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="956e5-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
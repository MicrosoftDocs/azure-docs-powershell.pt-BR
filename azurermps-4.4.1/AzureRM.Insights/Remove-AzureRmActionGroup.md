---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610499"
---
# <span data-ttu-id="1a657-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="1a657-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="1a657-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a657-102">SYNOPSIS</span></span>
<span data-ttu-id="1a657-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="1a657-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a657-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a657-104">SYNTAX</span></span>

### <span data-ttu-id="1a657-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a657-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a657-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a657-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a657-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a657-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a657-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a657-108">DESCRIPTION</span></span>
<span data-ttu-id="1a657-109">O cmdlet **Remove-AzureRmActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="1a657-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="1a657-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a657-110">EXAMPLES</span></span>

### <span data-ttu-id="1a657-111">Exemplo 1: remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="1a657-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="1a657-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a657-112">PARAMETERS</span></span>

### <span data-ttu-id="1a657-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a657-113">-Name</span></span>
<span data-ttu-id="1a657-114">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="1a657-114">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a657-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a657-115">-Confirm</span></span>
<span data-ttu-id="1a657-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a657-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a657-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a657-117">-DefaultProfile</span></span>
<span data-ttu-id="1a657-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a657-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a657-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a657-119">-InputObject</span></span>
<span data-ttu-id="1a657-120">O recurso grupo de ações</span><span class="sxs-lookup"><span data-stu-id="1a657-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a657-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a657-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a657-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1a657-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a657-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a657-123">-ResourceId</span></span>
<span data-ttu-id="1a657-124">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="1a657-124">The resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a657-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a657-125">-WhatIf</span></span>
<span data-ttu-id="1a657-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a657-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a657-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a657-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a657-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a657-128">CommonParameters</span></span>
<span data-ttu-id="1a657-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a657-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a657-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a657-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a657-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a657-131">INPUTS</span></span>

## <span data-ttu-id="1a657-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a657-132">OUTPUTS</span></span>

### <span data-ttu-id="1a657-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a657-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1a657-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a657-134">NOTES</span></span>

## <span data-ttu-id="1a657-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a657-135">RELATED LINKS</span></span>

<span data-ttu-id="1a657-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1a657-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>

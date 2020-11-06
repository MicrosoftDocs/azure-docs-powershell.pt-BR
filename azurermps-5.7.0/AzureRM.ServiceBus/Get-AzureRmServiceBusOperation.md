---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609935"
---
# <span data-ttu-id="4e2cf-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="4e2cf-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="4e2cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2cf-103">Lista de operações do ServiceBus com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2cf-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e2cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e2cf-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e2cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2cf-106">O cmdlet **Get-AzureRmServiceBusOperation** lista as operações com suporte do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4e2cf-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="4e2cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e2cf-107">EXAMPLES</span></span>

### <span data-ttu-id="4e2cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e2cf-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="4e2cf-109">Lista as operações com suporte do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4e2cf-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="4e2cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="4e2cf-110">PARAMETERS</span></span>

### <span data-ttu-id="4e2cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2cf-111">-DefaultProfile</span></span>
<span data-ttu-id="4e2cf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e2cf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e2cf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2cf-113">CommonParameters</span></span>
<span data-ttu-id="4e2cf-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e2cf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2cf-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2cf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2cf-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e2cf-116">INPUTS</span></span>

### <span data-ttu-id="4e2cf-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4e2cf-117">None</span></span>

### <span data-ttu-id="4e2cf-118">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. PSOperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4e2cf-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4e2cf-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e2cf-119">OUTPUTS</span></span>

### <span data-ttu-id="4e2cf-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. Operationattributes]</span><span class="sxs-lookup"><span data-stu-id="4e2cf-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="4e2cf-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e2cf-121">NOTES</span></span>

## <span data-ttu-id="4e2cf-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e2cf-122">RELATED LINKS</span></span>


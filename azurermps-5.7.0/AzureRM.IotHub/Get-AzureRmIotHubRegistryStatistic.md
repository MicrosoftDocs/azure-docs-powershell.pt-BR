---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: d9c53652dab75b342dbf410cae8e8968534afcc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440461"
---
# <span data-ttu-id="204de-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="204de-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="204de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="204de-102">SYNOPSIS</span></span>
<span data-ttu-id="204de-103">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="204de-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="204de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="204de-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="204de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="204de-105">DESCRIPTION</span></span>
<span data-ttu-id="204de-106">Obtém o RegistryStatistics de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="204de-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="204de-107">Isso fornece informações sobre o número total de dispositivos habilitados, habilitados e desativados em um IotHub.</span><span class="sxs-lookup"><span data-stu-id="204de-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="204de-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="204de-108">EXAMPLES</span></span>

### <span data-ttu-id="204de-109">Exemplo 1 obter o RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="204de-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="204de-110">Obtém o RegistryStatictics para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="204de-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="204de-111">OS</span><span class="sxs-lookup"><span data-stu-id="204de-111">PARAMETERS</span></span>

### <span data-ttu-id="204de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204de-112">-DefaultProfile</span></span>
<span data-ttu-id="204de-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="204de-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="204de-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="204de-114">-Name</span></span>
<span data-ttu-id="204de-115">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="204de-115">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204de-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="204de-116">-ResourceGroupName</span></span>
<span data-ttu-id="204de-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="204de-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204de-118">CommonParameters</span></span>
<span data-ttu-id="204de-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204de-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204de-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204de-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="204de-121">INPUTS</span></span>

### <span data-ttu-id="204de-122">System. String</span><span class="sxs-lookup"><span data-stu-id="204de-122">System.String</span></span>

## <span data-ttu-id="204de-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="204de-123">OUTPUTS</span></span>

### <span data-ttu-id="204de-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="204de-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="204de-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="204de-125">NOTES</span></span>

## <span data-ttu-id="204de-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="204de-126">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609386"
---
# <span data-ttu-id="1705a-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="1705a-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="1705a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1705a-102">SYNOPSIS</span></span>
<span data-ttu-id="1705a-103">Obter as delegações de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="1705a-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1705a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1705a-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1705a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1705a-105">DESCRIPTION</span></span>
<span data-ttu-id="1705a-106">O cmdlet **Get-AzureRmAvailableServiceDelegation** permite que você recupere todas as delegações de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="1705a-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="1705a-107">Esse cmdlet *não* descreve quais delegações podem coexistir em uma única sub-rede.</span><span class="sxs-lookup"><span data-stu-id="1705a-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="1705a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1705a-108">EXAMPLES</span></span>

### <span data-ttu-id="1705a-109">1: obtendo todas as delegação de serviços disponíveis</span><span class="sxs-lookup"><span data-stu-id="1705a-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="1705a-110">OS</span><span class="sxs-lookup"><span data-stu-id="1705a-110">PARAMETERS</span></span>

### <span data-ttu-id="1705a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1705a-111">-DefaultProfile</span></span>
<span data-ttu-id="1705a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1705a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1705a-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1705a-113">-Location</span></span>
<span data-ttu-id="1705a-114">O local.</span><span class="sxs-lookup"><span data-stu-id="1705a-114">The location.</span></span>

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

### <span data-ttu-id="1705a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1705a-115">CommonParameters</span></span>
<span data-ttu-id="1705a-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1705a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1705a-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1705a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1705a-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1705a-118">INPUTS</span></span>

### <span data-ttu-id="1705a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1705a-119">System.String</span></span>

## <span data-ttu-id="1705a-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1705a-120">OUTPUTS</span></span>

### <span data-ttu-id="1705a-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="1705a-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="1705a-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1705a-122">NOTES</span></span>

## <span data-ttu-id="1705a-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1705a-123">RELATED LINKS</span></span>
<span data-ttu-id="1705a-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="1705a-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>

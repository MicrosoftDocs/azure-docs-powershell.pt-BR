---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111113"
---
# <span data-ttu-id="02937-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="02937-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="02937-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02937-102">SYNOPSIS</span></span>
<span data-ttu-id="02937-103">Obter as delegações de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="02937-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="02937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02937-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02937-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02937-105">DESCRIPTION</span></span>
<span data-ttu-id="02937-106">O cmdlet **Get-AzAvailableServiceDelegation** permite que você recupere todas as delegações de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="02937-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="02937-107">Esse cmdlet *não* descreve quais delegações podem coexistir em uma única sub-rede.</span><span class="sxs-lookup"><span data-stu-id="02937-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="02937-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02937-108">EXAMPLES</span></span>

### <span data-ttu-id="02937-109">1: obtendo todas as delegação de serviços disponíveis</span><span class="sxs-lookup"><span data-stu-id="02937-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="02937-110">OS</span><span class="sxs-lookup"><span data-stu-id="02937-110">PARAMETERS</span></span>

### <span data-ttu-id="02937-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02937-111">-DefaultProfile</span></span>
<span data-ttu-id="02937-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02937-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02937-113">-Local</span><span class="sxs-lookup"><span data-stu-id="02937-113">-Location</span></span>
<span data-ttu-id="02937-114">O local.</span><span class="sxs-lookup"><span data-stu-id="02937-114">The location.</span></span>

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

### <span data-ttu-id="02937-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02937-115">CommonParameters</span></span>
<span data-ttu-id="02937-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02937-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02937-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02937-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02937-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02937-118">INPUTS</span></span>

### <span data-ttu-id="02937-119">System. String</span><span class="sxs-lookup"><span data-stu-id="02937-119">System.String</span></span>

## <span data-ttu-id="02937-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02937-120">OUTPUTS</span></span>

### <span data-ttu-id="02937-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="02937-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="02937-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02937-122">NOTES</span></span>

## <span data-ttu-id="02937-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02937-123">RELATED LINKS</span></span>

<span data-ttu-id="02937-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="02937-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>
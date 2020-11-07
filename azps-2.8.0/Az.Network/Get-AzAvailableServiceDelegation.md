---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 547069954ada24531e1551b75c4065416eeae1fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772042"
---
# <span data-ttu-id="d0a48-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="d0a48-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="d0a48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0a48-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a48-103">Obter as delegações de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="d0a48-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="d0a48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0a48-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0a48-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a48-106">O cmdlet **Get-AzAvailableServiceDelegation** permite que você recupere todas as delegações de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="d0a48-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="d0a48-107">Esse cmdlet *não* descreve quais delegações podem coexistir em uma única sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d0a48-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="d0a48-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0a48-108">EXAMPLES</span></span>

### <span data-ttu-id="d0a48-109">1: obtendo todas as delegação de serviços disponíveis</span><span class="sxs-lookup"><span data-stu-id="d0a48-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="d0a48-110">OS</span><span class="sxs-lookup"><span data-stu-id="d0a48-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a48-111">-DefaultProfile</span></span>
<span data-ttu-id="d0a48-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a48-113">-Local</span><span class="sxs-lookup"><span data-stu-id="d0a48-113">-Location</span></span>
<span data-ttu-id="d0a48-114">O local.</span><span class="sxs-lookup"><span data-stu-id="d0a48-114">The location.</span></span>

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

### <span data-ttu-id="d0a48-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a48-115">CommonParameters</span></span>
<span data-ttu-id="d0a48-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a48-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a48-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0a48-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a48-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0a48-118">INPUTS</span></span>

### <span data-ttu-id="d0a48-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a48-119">System.String</span></span>

## <span data-ttu-id="d0a48-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0a48-120">OUTPUTS</span></span>

### <span data-ttu-id="d0a48-121">Microsoft. Azure. Commands. Network. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="d0a48-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="d0a48-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0a48-122">NOTES</span></span>

## <span data-ttu-id="d0a48-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0a48-123">RELATED LINKS</span></span>

<span data-ttu-id="d0a48-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="d0a48-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>
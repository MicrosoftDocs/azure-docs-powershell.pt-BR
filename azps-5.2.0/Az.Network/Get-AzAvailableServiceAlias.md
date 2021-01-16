---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259063"
---
# <span data-ttu-id="a342f-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="a342f-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="a342f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a342f-102">SYNOPSIS</span></span>
<span data-ttu-id="a342f-103">Obter aliases de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="a342f-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="a342f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a342f-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a342f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a342f-105">DESCRIPTION</span></span>
<span data-ttu-id="a342f-106">O cmdlet **Get-AzAvailableServiceAlias** permite que você recupere todos os aliases de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="a342f-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="a342f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a342f-107">EXAMPLES</span></span>

### <span data-ttu-id="a342f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a342f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="a342f-109">OS</span><span class="sxs-lookup"><span data-stu-id="a342f-109">PARAMETERS</span></span>

### <span data-ttu-id="a342f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a342f-110">-DefaultProfile</span></span>
<span data-ttu-id="a342f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a342f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a342f-112">-Local</span><span class="sxs-lookup"><span data-stu-id="a342f-112">-Location</span></span>
<span data-ttu-id="a342f-113">O local.</span><span class="sxs-lookup"><span data-stu-id="a342f-113">The location.</span></span>

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

### <span data-ttu-id="a342f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a342f-114">CommonParameters</span></span>
<span data-ttu-id="a342f-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a342f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a342f-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a342f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a342f-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a342f-117">INPUTS</span></span>

### <span data-ttu-id="a342f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="a342f-118">System.String</span></span>

## <span data-ttu-id="a342f-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a342f-119">OUTPUTS</span></span>

### <span data-ttu-id="a342f-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="a342f-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="a342f-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a342f-121">NOTES</span></span>

## <span data-ttu-id="a342f-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a342f-122">RELATED LINKS</span></span>

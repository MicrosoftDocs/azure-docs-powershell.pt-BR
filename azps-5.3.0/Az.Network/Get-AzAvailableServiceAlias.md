---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428153"
---
# <span data-ttu-id="91dc8-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="91dc8-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="91dc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="91dc8-103">Obter aliases de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="91dc8-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="91dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91dc8-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91dc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="91dc8-106">O cmdlet **Get-AzAvailableServiceAlias** permite que você recupere todos os aliases de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="91dc8-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="91dc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="91dc8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91dc8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="91dc8-109">OS</span><span class="sxs-lookup"><span data-stu-id="91dc8-109">PARAMETERS</span></span>

### <span data-ttu-id="91dc8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dc8-110">-DefaultProfile</span></span>
<span data-ttu-id="91dc8-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91dc8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91dc8-112">-Local</span><span class="sxs-lookup"><span data-stu-id="91dc8-112">-Location</span></span>
<span data-ttu-id="91dc8-113">O local.</span><span class="sxs-lookup"><span data-stu-id="91dc8-113">The location.</span></span>

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

### <span data-ttu-id="91dc8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dc8-114">CommonParameters</span></span>
<span data-ttu-id="91dc8-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91dc8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dc8-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91dc8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dc8-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91dc8-117">INPUTS</span></span>

### <span data-ttu-id="91dc8-118">System. String</span><span class="sxs-lookup"><span data-stu-id="91dc8-118">System.String</span></span>

## <span data-ttu-id="91dc8-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91dc8-119">OUTPUTS</span></span>

### <span data-ttu-id="91dc8-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="91dc8-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="91dc8-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91dc8-121">NOTES</span></span>

## <span data-ttu-id="91dc8-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91dc8-122">RELATED LINKS</span></span>

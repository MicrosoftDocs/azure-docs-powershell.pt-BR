---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115191"
---
# <span data-ttu-id="2c564-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="2c564-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="2c564-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c564-102">SYNOPSIS</span></span>
<span data-ttu-id="2c564-103">Obter aliases de serviço disponíveis na região.</span><span class="sxs-lookup"><span data-stu-id="2c564-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="2c564-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c564-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c564-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c564-105">DESCRIPTION</span></span>
<span data-ttu-id="2c564-106">O cmdlet **Get-AzAvailableServiceAlias** permite recuperar todos os aliases de serviço disponíveis para uma sub-rede no local fornecido.</span><span class="sxs-lookup"><span data-stu-id="2c564-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="2c564-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c564-107">EXAMPLES</span></span>

### <span data-ttu-id="2c564-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c564-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="2c564-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c564-109">PARAMETERS</span></span>

### <span data-ttu-id="2c564-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c564-110">-DefaultProfile</span></span>
<span data-ttu-id="2c564-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c564-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c564-112">-Local</span><span class="sxs-lookup"><span data-stu-id="2c564-112">-Location</span></span>
<span data-ttu-id="2c564-113">O local.</span><span class="sxs-lookup"><span data-stu-id="2c564-113">The location.</span></span>

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

### <span data-ttu-id="2c564-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c564-114">CommonParameters</span></span>
<span data-ttu-id="2c564-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c564-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c564-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c564-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c564-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c564-117">INPUTS</span></span>

### <span data-ttu-id="2c564-118">System.String</span><span class="sxs-lookup"><span data-stu-id="2c564-118">System.String</span></span>

## <span data-ttu-id="2c564-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c564-119">OUTPUTS</span></span>

### <span data-ttu-id="2c564-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="2c564-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="2c564-121">Notas</span><span class="sxs-lookup"><span data-stu-id="2c564-121">NOTES</span></span>

## <span data-ttu-id="2c564-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c564-122">RELATED LINKS</span></span>

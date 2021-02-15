---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113767"
---
# <span data-ttu-id="8a8d3-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="8a8d3-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="8a8d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8d3-103">Obtém todas as SKIs válidas para as que este IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="8a8d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a8d3-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8d3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a8d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8d3-106">Obtém todas as SKU válidas para as que este IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="8a8d3-107">Um IotHub não pode fazer a transição entre as SKUs gratuitas e pagas e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="8a8d3-108">Você terá que excluir e recriar o iothub se quiser fazer isso.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="8a8d3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a8d3-109">EXAMPLES</span></span>

### <span data-ttu-id="8a8d3-110">Exemplo 1 Obter as SKUs válidas</span><span class="sxs-lookup"><span data-stu-id="8a8d3-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8a8d3-111">Obtém uma lista de todas as skks do IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8a8d3-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8a8d3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a8d3-112">PARAMETERS</span></span>

### <span data-ttu-id="8a8d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8d3-113">-DefaultProfile</span></span>
<span data-ttu-id="8a8d3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8a8d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a8d3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a8d3-115">-Name</span></span>
<span data-ttu-id="8a8d3-116">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a8d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a8d3-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8a8d3-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8d3-119">CommonParameters</span></span>
<span data-ttu-id="8a8d3-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8d3-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8d3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8d3-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a8d3-122">INPUTS</span></span>

### <span data-ttu-id="8a8d3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8a8d3-123">System.String</span></span>

## <span data-ttu-id="8a8d3-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a8d3-124">OUTPUTS</span></span>

### <span data-ttu-id="8a8d3-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="8a8d3-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="8a8d3-126">Notas</span><span class="sxs-lookup"><span data-stu-id="8a8d3-126">NOTES</span></span>

## <span data-ttu-id="8a8d3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a8d3-127">RELATED LINKS</span></span>

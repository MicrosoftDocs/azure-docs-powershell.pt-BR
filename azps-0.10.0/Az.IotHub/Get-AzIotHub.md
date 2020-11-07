---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 1076ff16005665aa81e4775507a236fe62bb0965
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776703"
---
# <span data-ttu-id="44faf-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="44faf-101">Get-AzIotHub</span></span>

## <span data-ttu-id="44faf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44faf-102">SYNOPSIS</span></span>
<span data-ttu-id="44faf-103">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="44faf-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="44faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44faf-104">SYNTAX</span></span>

### <span data-ttu-id="44faf-105">ListIotHubsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="44faf-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44faf-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="44faf-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44faf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44faf-107">DESCRIPTION</span></span>
<span data-ttu-id="44faf-108">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="44faf-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="44faf-109">Você pode exibir todas as instâncias de IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome de IotHub específico.</span><span class="sxs-lookup"><span data-stu-id="44faf-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="44faf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44faf-110">EXAMPLES</span></span>

### <span data-ttu-id="44faf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44faf-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="44faf-112">Obtém todas as IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="44faf-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="44faf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44faf-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="44faf-114">Obtém todos os IotHubs na assinatura pertencente ao The Resource, chamado "myresourceus".</span><span class="sxs-lookup"><span data-stu-id="44faf-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="44faf-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="44faf-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="44faf-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="44faf-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="44faf-117">OS</span><span class="sxs-lookup"><span data-stu-id="44faf-117">PARAMETERS</span></span>

### <span data-ttu-id="44faf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44faf-118">-DefaultProfile</span></span>
<span data-ttu-id="44faf-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="44faf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44faf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="44faf-120">-Name</span></span>
<span data-ttu-id="44faf-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="44faf-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44faf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44faf-122">-ResourceGroupName</span></span>
<span data-ttu-id="44faf-123">Nome do The Resource</span><span class="sxs-lookup"><span data-stu-id="44faf-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44faf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44faf-124">CommonParameters</span></span>
<span data-ttu-id="44faf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44faf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44faf-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44faf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44faf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44faf-127">INPUTS</span></span>

### <span data-ttu-id="44faf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44faf-128">System.String</span></span>

## <span data-ttu-id="44faf-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44faf-129">OUTPUTS</span></span>

### <span data-ttu-id="44faf-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="44faf-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="44faf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44faf-131">NOTES</span></span>

## <span data-ttu-id="44faf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44faf-132">RELATED LINKS</span></span>

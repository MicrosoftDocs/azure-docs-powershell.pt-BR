---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440414"
---
# <span data-ttu-id="d96c5-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d96c5-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="d96c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d96c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d96c5-103">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="d96c5-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d96c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d96c5-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d96c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d96c5-106">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="d96c5-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="d96c5-107">Você pode listar todas as chaves ou filtrar a lista por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="d96c5-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="d96c5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d96c5-108">EXAMPLES</span></span>

### <span data-ttu-id="d96c5-109">Exemplo 1 obter todas as chaves</span><span class="sxs-lookup"><span data-stu-id="d96c5-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d96c5-110">Obtém todas as chaves para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d96c5-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d96c5-111">Exemplo 2 obter informações para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="d96c5-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="d96c5-112">Obtém as informações de uma chave chamada "iothubowner" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d96c5-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d96c5-113">OS</span><span class="sxs-lookup"><span data-stu-id="d96c5-113">PARAMETERS</span></span>

### <span data-ttu-id="d96c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96c5-114">-DefaultProfile</span></span>
<span data-ttu-id="d96c5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d96c5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96c5-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d96c5-116">-KeyName</span></span>
<span data-ttu-id="d96c5-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="d96c5-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96c5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d96c5-118">-Name</span></span>
<span data-ttu-id="d96c5-119">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d96c5-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d96c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="d96c5-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d96c5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d96c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96c5-122">CommonParameters</span></span>
<span data-ttu-id="d96c5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96c5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96c5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d96c5-125">INPUTS</span></span>

### <span data-ttu-id="d96c5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d96c5-126">System.String</span></span>

## <span data-ttu-id="d96c5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d96c5-127">OUTPUTS</span></span>

### <span data-ttu-id="d96c5-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d96c5-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d96c5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d96c5-129">NOTES</span></span>

## <span data-ttu-id="d96c5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d96c5-130">RELATED LINKS</span></span>

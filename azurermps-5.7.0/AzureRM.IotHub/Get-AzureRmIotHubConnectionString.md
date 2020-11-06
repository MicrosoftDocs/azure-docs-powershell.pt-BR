---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430465"
---
# <span data-ttu-id="90fce-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="90fce-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="90fce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90fce-102">SYNOPSIS</span></span>
<span data-ttu-id="90fce-103">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="90fce-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90fce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90fce-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90fce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90fce-105">DESCRIPTION</span></span>
<span data-ttu-id="90fce-106">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="90fce-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="90fce-107">Você pode obter connectionStrings para todas as chaves ou filtrá-las por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="90fce-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="90fce-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90fce-108">EXAMPLES</span></span>

### <span data-ttu-id="90fce-109">Exemplo 1 obter todos os connectionStrings IotHub</span><span class="sxs-lookup"><span data-stu-id="90fce-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="90fce-110">Obtém as connectionStrings para todas as chaves para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="90fce-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="90fce-111">Exemplo 2 obter os connectionStrings IotHub para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="90fce-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="90fce-112">Obtém as connectionStrings para a chave chamada "myKey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="90fce-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="90fce-113">OS</span><span class="sxs-lookup"><span data-stu-id="90fce-113">PARAMETERS</span></span>

### <span data-ttu-id="90fce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fce-114">-DefaultProfile</span></span>
<span data-ttu-id="90fce-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="90fce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90fce-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="90fce-116">-KeyName</span></span>
<span data-ttu-id="90fce-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="90fce-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fce-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="90fce-118">-Name</span></span>
<span data-ttu-id="90fce-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="90fce-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="90fce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90fce-120">-ResourceGroupName</span></span>
<span data-ttu-id="90fce-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="90fce-121">Resource Group Name</span></span>

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

### <span data-ttu-id="90fce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fce-122">CommonParameters</span></span>
<span data-ttu-id="90fce-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90fce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fce-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fce-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90fce-125">INPUTS</span></span>

### <span data-ttu-id="90fce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="90fce-126">System.String</span></span>

## <span data-ttu-id="90fce-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90fce-127">OUTPUTS</span></span>

### <span data-ttu-id="90fce-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="90fce-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="90fce-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="90fce-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="90fce-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90fce-130">NOTES</span></span>

## <span data-ttu-id="90fce-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90fce-131">RELATED LINKS</span></span>


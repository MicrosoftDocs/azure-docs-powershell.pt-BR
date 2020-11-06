---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 6e56bab4fb17aa485a1103a2be3a8b5592fc4393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440415"
---
# <span data-ttu-id="f46a1-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="f46a1-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="f46a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f46a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f46a1-103">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="f46a1-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f46a1-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f46a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f46a1-106">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="f46a1-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="f46a1-107">Você pode obter connectionStrings para todas as chaves ou filtrá-las por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="f46a1-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="f46a1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f46a1-108">EXAMPLES</span></span>

### <span data-ttu-id="f46a1-109">Exemplo 1 obter todos os connectionStrings IotHub</span><span class="sxs-lookup"><span data-stu-id="f46a1-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f46a1-110">Obtém as connectionStrings para todas as chaves para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f46a1-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="f46a1-111">Exemplo 2 obter os connectionStrings IotHub para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="f46a1-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="f46a1-112">Obtém as connectionStrings para a chave chamada "myKey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f46a1-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="f46a1-113">OS</span><span class="sxs-lookup"><span data-stu-id="f46a1-113">PARAMETERS</span></span>

### <span data-ttu-id="f46a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46a1-114">-DefaultProfile</span></span>
<span data-ttu-id="f46a1-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f46a1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f46a1-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f46a1-116">-KeyName</span></span>
<span data-ttu-id="f46a1-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f46a1-117">Name of the Key</span></span>

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

### <span data-ttu-id="f46a1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f46a1-118">-Name</span></span>
<span data-ttu-id="f46a1-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="f46a1-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f46a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="f46a1-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f46a1-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f46a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46a1-122">CommonParameters</span></span>
<span data-ttu-id="f46a1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46a1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46a1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f46a1-125">INPUTS</span></span>

### <span data-ttu-id="f46a1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f46a1-126">System.String</span></span>

## <span data-ttu-id="f46a1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f46a1-127">OUTPUTS</span></span>

### <span data-ttu-id="f46a1-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f46a1-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="f46a1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f46a1-129">NOTES</span></span>

## <span data-ttu-id="f46a1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f46a1-130">RELATED LINKS</span></span>

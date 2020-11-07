---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770730"
---
# <span data-ttu-id="337d9-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="337d9-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="337d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="337d9-102">SYNOPSIS</span></span>
<span data-ttu-id="337d9-103">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="337d9-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="337d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="337d9-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="337d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="337d9-105">DESCRIPTION</span></span>
<span data-ttu-id="337d9-106">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="337d9-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="337d9-107">Você pode obter connectionStrings para todas as chaves ou filtrá-las por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="337d9-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="337d9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="337d9-108">EXAMPLES</span></span>

### <span data-ttu-id="337d9-109">Exemplo 1 obter todos os connectionStrings IotHub</span><span class="sxs-lookup"><span data-stu-id="337d9-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="337d9-110">Obtém as connectionStrings para todas as chaves para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="337d9-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="337d9-111">Exemplo 2 obter os connectionStrings IotHub para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="337d9-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="337d9-112">Obtém as connectionStrings para a chave chamada "myKey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="337d9-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="337d9-113">OS</span><span class="sxs-lookup"><span data-stu-id="337d9-113">PARAMETERS</span></span>

### <span data-ttu-id="337d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337d9-114">-DefaultProfile</span></span>
<span data-ttu-id="337d9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="337d9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="337d9-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="337d9-116">-KeyName</span></span>
<span data-ttu-id="337d9-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="337d9-117">Name of the Key</span></span>

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

### <span data-ttu-id="337d9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="337d9-118">-Name</span></span>
<span data-ttu-id="337d9-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="337d9-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="337d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="337d9-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="337d9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="337d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337d9-122">CommonParameters</span></span>
<span data-ttu-id="337d9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337d9-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337d9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337d9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="337d9-125">INPUTS</span></span>

### <span data-ttu-id="337d9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="337d9-126">System.String</span></span>

## <span data-ttu-id="337d9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="337d9-127">OUTPUTS</span></span>

### <span data-ttu-id="337d9-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="337d9-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="337d9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="337d9-129">NOTES</span></span>

## <span data-ttu-id="337d9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="337d9-130">RELATED LINKS</span></span>

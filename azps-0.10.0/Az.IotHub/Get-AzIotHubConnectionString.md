---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: 92d1e3f2ef1ba87a5e9683f7ac6617e31bb8a055
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775844"
---
# <span data-ttu-id="daf4d-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="daf4d-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="daf4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="daf4d-103">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="daf4d-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="daf4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daf4d-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daf4d-105">DESCRIPTION</span></span>
<span data-ttu-id="daf4d-106">Obtém os connectionStrings IotHub.</span><span class="sxs-lookup"><span data-stu-id="daf4d-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="daf4d-107">Você pode obter connectionStrings para todas as chaves ou filtrá-las por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="daf4d-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="daf4d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daf4d-108">EXAMPLES</span></span>

### <span data-ttu-id="daf4d-109">Exemplo 1 obter todos os connectionStrings IotHub</span><span class="sxs-lookup"><span data-stu-id="daf4d-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="daf4d-110">Obtém as connectionStrings para todas as chaves para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="daf4d-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="daf4d-111">Exemplo 2 obter os connectionStrings IotHub para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="daf4d-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="daf4d-112">Obtém as connectionStrings para a chave chamada "myKey" para o iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="daf4d-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="daf4d-113">OS</span><span class="sxs-lookup"><span data-stu-id="daf4d-113">PARAMETERS</span></span>

### <span data-ttu-id="daf4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf4d-114">-DefaultProfile</span></span>
<span data-ttu-id="daf4d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="daf4d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daf4d-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="daf4d-116">-KeyName</span></span>
<span data-ttu-id="daf4d-117">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="daf4d-117">Name of the Key</span></span>

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

### <span data-ttu-id="daf4d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="daf4d-118">-Name</span></span>
<span data-ttu-id="daf4d-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="daf4d-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="daf4d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf4d-120">-ResourceGroupName</span></span>
<span data-ttu-id="daf4d-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="daf4d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="daf4d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf4d-122">CommonParameters</span></span>
<span data-ttu-id="daf4d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf4d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf4d-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf4d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf4d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daf4d-125">INPUTS</span></span>

### <span data-ttu-id="daf4d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="daf4d-126">System.String</span></span>

## <span data-ttu-id="daf4d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daf4d-127">OUTPUTS</span></span>

### <span data-ttu-id="daf4d-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="daf4d-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="daf4d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daf4d-129">NOTES</span></span>

## <span data-ttu-id="daf4d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daf4d-130">RELATED LINKS</span></span>

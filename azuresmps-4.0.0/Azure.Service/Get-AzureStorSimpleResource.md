---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945554"
---
# <span data-ttu-id="78a55-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="78a55-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="78a55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78a55-102">SYNOPSIS</span></span>
<span data-ttu-id="78a55-103">Obtém todos os recursos que você criou.</span><span class="sxs-lookup"><span data-stu-id="78a55-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="78a55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78a55-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78a55-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78a55-105">DESCRIPTION</span></span>
<span data-ttu-id="78a55-106">O cmdlet **Get-AzureStorSimpleResource** Obtém todos os recursos que você criou usando o portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="78a55-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="78a55-107">O cmdlet obtém detalhes que você pode usar para se conectar aos recursos.</span><span class="sxs-lookup"><span data-stu-id="78a55-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="78a55-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78a55-108">EXAMPLES</span></span>

### <span data-ttu-id="78a55-109">Exemplo 1: obter todos os recursos</span><span class="sxs-lookup"><span data-stu-id="78a55-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="78a55-110">Esse comando obtém todos os recursos que você criou.</span><span class="sxs-lookup"><span data-stu-id="78a55-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="78a55-111">Neste exemplo, há três recursos.</span><span class="sxs-lookup"><span data-stu-id="78a55-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="78a55-112">Exemplo 2: obter um recurso usando seu nome</span><span class="sxs-lookup"><span data-stu-id="78a55-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="78a55-113">Esse comando obtém o recurso chamado Contoso63-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="78a55-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="78a55-114">Exemplo 3: tentativa de obter um recurso inexistente</span><span class="sxs-lookup"><span data-stu-id="78a55-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="78a55-115">Esse comando tenta obter o recurso chamado Contoso64-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="78a55-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="78a55-116">Não há nenhum recurso com esse nome.</span><span class="sxs-lookup"><span data-stu-id="78a55-116">There is no resource that has this name.</span></span>
<span data-ttu-id="78a55-117">Este exemplo não retorna nenhum recurso.</span><span class="sxs-lookup"><span data-stu-id="78a55-117">This example does not return any resource.</span></span>

## <span data-ttu-id="78a55-118">OS</span><span class="sxs-lookup"><span data-stu-id="78a55-118">PARAMETERS</span></span>

### <span data-ttu-id="78a55-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="78a55-119">-Profile</span></span>
<span data-ttu-id="78a55-120">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="78a55-120">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a55-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="78a55-121">-ResourceName</span></span>
<span data-ttu-id="78a55-122">Especifica o nome do recurso que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78a55-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a55-123">CommonParameters</span></span>
<span data-ttu-id="78a55-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a55-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a55-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a55-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78a55-126">INPUTS</span></span>

### <span data-ttu-id="78a55-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="78a55-127">None</span></span>

## <span data-ttu-id="78a55-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78a55-128">OUTPUTS</span></span>

### <span data-ttu-id="78a55-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="78a55-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="78a55-130">Esse cmdlet retorna objetos **ResourceCredentials** que contêm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="78a55-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="78a55-131">**Source**</span><span class="sxs-lookup"><span data-stu-id="78a55-131">**ResourceName**</span></span>
- <span data-ttu-id="78a55-132">**Retanto**</span><span class="sxs-lookup"><span data-stu-id="78a55-132">**ResouceId**</span></span>
- <span data-ttu-id="78a55-133">**Resourcestate**</span><span class="sxs-lookup"><span data-stu-id="78a55-133">**ResourceState**</span></span>

## <span data-ttu-id="78a55-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78a55-134">NOTES</span></span>

## <span data-ttu-id="78a55-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78a55-135">RELATED LINKS</span></span>

[<span data-ttu-id="78a55-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="78a55-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="78a55-137">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="78a55-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)



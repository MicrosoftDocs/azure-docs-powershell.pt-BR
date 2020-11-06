---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426149"
---
# <span data-ttu-id="f048a-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f048a-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="f048a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f048a-102">SYNOPSIS</span></span>
<span data-ttu-id="f048a-103">Obtém Propriedades de registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f048a-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="f048a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f048a-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="f048a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f048a-105">DESCRIPTION</span></span>
<span data-ttu-id="f048a-106">O cmdlet **Get-AzureStorageServiceLoggingProperty** Obtém Propriedades de log para os serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f048a-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="f048a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f048a-107">EXAMPLES</span></span>

### <span data-ttu-id="f048a-108">Exemplo 1: obter propriedades de log para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="f048a-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="f048a-109">Este comando obtém Propriedades de log para armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="f048a-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="f048a-110">OS</span><span class="sxs-lookup"><span data-stu-id="f048a-110">PARAMETERS</span></span>

### <span data-ttu-id="f048a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f048a-111">-Context</span></span>
<span data-ttu-id="f048a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f048a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f048a-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f048a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f048a-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f048a-114">-ServiceType</span></span>
<span data-ttu-id="f048a-115">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f048a-115">Specifies the storage service type.</span></span>
<span data-ttu-id="f048a-116">Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f048a-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f048a-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f048a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f048a-118">Irregular</span><span class="sxs-lookup"><span data-stu-id="f048a-118">Blob</span></span> 
- <span data-ttu-id="f048a-119">TableName</span><span class="sxs-lookup"><span data-stu-id="f048a-119">Table</span></span>
- <span data-ttu-id="f048a-120">Coloca</span><span class="sxs-lookup"><span data-stu-id="f048a-120">Queue</span></span>
- <span data-ttu-id="f048a-121">Arquivos</span><span class="sxs-lookup"><span data-stu-id="f048a-121">File</span></span>

<span data-ttu-id="f048a-122">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="f048a-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f048a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f048a-123">CommonParameters</span></span>
<span data-ttu-id="f048a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f048a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f048a-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f048a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f048a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f048a-126">INPUTS</span></span>

## <span data-ttu-id="f048a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f048a-127">OUTPUTS</span></span>

## <span data-ttu-id="f048a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f048a-128">NOTES</span></span>

## <span data-ttu-id="f048a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f048a-129">RELATED LINKS</span></span>

[<span data-ttu-id="f048a-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f048a-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f048a-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f048a-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)



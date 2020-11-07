---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946850"
---
# <span data-ttu-id="96e12-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="96e12-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="96e12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96e12-102">SYNOPSIS</span></span>
<span data-ttu-id="96e12-103">Locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="96e12-103">Directory tenant.</span></span>

## <span data-ttu-id="96e12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96e12-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="96e12-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96e12-105">DESCRIPTION</span></span>
<span data-ttu-id="96e12-106">Locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="96e12-106">Directory tenant.</span></span>

## <span data-ttu-id="96e12-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96e12-107">EXAMPLES</span></span>

### <span data-ttu-id="96e12-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96e12-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="96e12-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="96e12-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="96e12-110">OS</span><span class="sxs-lookup"><span data-stu-id="96e12-110">PARAMETERS</span></span>

### <span data-ttu-id="96e12-111">-ID</span><span class="sxs-lookup"><span data-stu-id="96e12-111">-Id</span></span>
<span data-ttu-id="96e12-112">URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e12-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e12-113">-Local</span><span class="sxs-lookup"><span data-stu-id="96e12-113">-Location</span></span>
<span data-ttu-id="96e12-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e12-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e12-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="96e12-115">-Name</span></span>
<span data-ttu-id="96e12-116">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="96e12-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e12-117">-Marcas</span><span class="sxs-lookup"><span data-stu-id="96e12-117">-Tags</span></span>
<span data-ttu-id="96e12-118">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="96e12-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e12-119">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="96e12-119">-TenantId</span></span>
<span data-ttu-id="96e12-120">Identificador exclusivo do locatário.</span><span class="sxs-lookup"><span data-stu-id="96e12-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e12-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="96e12-121">-Type</span></span>
<span data-ttu-id="96e12-122">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="96e12-122">Type of resource.</span></span>

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

### <span data-ttu-id="96e12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e12-123">CommonParameters</span></span>
<span data-ttu-id="96e12-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e12-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e12-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e12-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96e12-126">INPUTS</span></span>

## <span data-ttu-id="96e12-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96e12-127">OUTPUTS</span></span>

## <span data-ttu-id="96e12-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96e12-128">NOTES</span></span>

## <span data-ttu-id="96e12-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96e12-129">RELATED LINKS</span></span>


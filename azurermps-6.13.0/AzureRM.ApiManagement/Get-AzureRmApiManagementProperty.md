---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426512"
---
# <span data-ttu-id="f840e-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="f840e-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="f840e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f840e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f840e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f840e-103">SYNTAX</span></span>

### <span data-ttu-id="f840e-104">GetAllProperties (padrão)</span><span class="sxs-lookup"><span data-stu-id="f840e-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f840e-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="f840e-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840e-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="f840e-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f840e-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="f840e-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f840e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f840e-108">DESCRIPTION</span></span>

## <span data-ttu-id="f840e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f840e-109">EXAMPLES</span></span>

### <span data-ttu-id="f840e-110">Exemplo 1: obter propriedade por nome</span><span class="sxs-lookup"><span data-stu-id="f840e-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="f840e-111">OS</span><span class="sxs-lookup"><span data-stu-id="f840e-111">PARAMETERS</span></span>

### <span data-ttu-id="f840e-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f840e-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f840e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f840e-113">-DefaultProfile</span></span>
<span data-ttu-id="f840e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f840e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f840e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f840e-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f840e-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="f840e-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f840e-117">-Marca</span><span class="sxs-lookup"><span data-stu-id="f840e-117">-Tag</span></span>
<span data-ttu-id="f840e-118">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f840e-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f840e-119">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f840e-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f840e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f840e-120">CommonParameters</span></span>
<span data-ttu-id="f840e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f840e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f840e-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f840e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f840e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f840e-123">INPUTS</span></span>

### <span data-ttu-id="f840e-124">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f840e-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f840e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f840e-125">System.String</span></span>

## <span data-ttu-id="f840e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f840e-126">OUTPUTS</span></span>

### <span data-ttu-id="f840e-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="f840e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="f840e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f840e-128">NOTES</span></span>

## <span data-ttu-id="f840e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f840e-129">RELATED LINKS</span></span>

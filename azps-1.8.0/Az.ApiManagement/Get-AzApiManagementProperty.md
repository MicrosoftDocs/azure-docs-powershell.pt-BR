---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595670"
---
# <span data-ttu-id="358a7-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="358a7-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="358a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="358a7-102">SYNOPSIS</span></span>
<span data-ttu-id="358a7-103">Obtém uma lista ou uma propriedade específica (nome-valor).</span><span class="sxs-lookup"><span data-stu-id="358a7-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="358a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="358a7-104">SYNTAX</span></span>

### <span data-ttu-id="358a7-105">GetAllProperties (padrão)</span><span class="sxs-lookup"><span data-stu-id="358a7-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="358a7-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="358a7-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="358a7-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="358a7-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="358a7-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="358a7-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="358a7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="358a7-109">DESCRIPTION</span></span>
<span data-ttu-id="358a7-110">O cmdlet **Get-AzApiManagementProperty** Obtém uma lista ou uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="358a7-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="358a7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="358a7-111">EXAMPLES</span></span>

### <span data-ttu-id="358a7-112">Exemplo 1: obter propriedade por nome</span><span class="sxs-lookup"><span data-stu-id="358a7-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="358a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="358a7-113">PARAMETERS</span></span>

### <span data-ttu-id="358a7-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="358a7-114">-Context</span></span>
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

### <span data-ttu-id="358a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358a7-115">-DefaultProfile</span></span>
<span data-ttu-id="358a7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="358a7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="358a7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="358a7-117">-Name</span></span>
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

### <span data-ttu-id="358a7-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="358a7-118">-PropertyId</span></span>
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

### <span data-ttu-id="358a7-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="358a7-119">-Tag</span></span>
<span data-ttu-id="358a7-120">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="358a7-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="358a7-121">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="358a7-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="358a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358a7-122">CommonParameters</span></span>
<span data-ttu-id="358a7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358a7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358a7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="358a7-125">INPUTS</span></span>

### <span data-ttu-id="358a7-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="358a7-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="358a7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="358a7-127">System.String</span></span>

## <span data-ttu-id="358a7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="358a7-128">OUTPUTS</span></span>

### <span data-ttu-id="358a7-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="358a7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="358a7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="358a7-130">NOTES</span></span>

## <span data-ttu-id="358a7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="358a7-131">RELATED LINKS</span></span>

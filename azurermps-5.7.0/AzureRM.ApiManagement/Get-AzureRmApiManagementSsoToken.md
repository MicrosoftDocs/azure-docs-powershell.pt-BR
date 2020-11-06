---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429921"
---
# <span data-ttu-id="080db-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="080db-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="080db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="080db-102">SYNOPSIS</span></span>
<span data-ttu-id="080db-103">Obtém um link com um token de SSO para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="080db-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="080db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="080db-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="080db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="080db-105">DESCRIPTION</span></span>
<span data-ttu-id="080db-106">O cmdlet **Get-AzureRmApiManagementSsoToken** retorna um link (URL) que contém um token de logon único (SSO) para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="080db-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="080db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="080db-107">EXAMPLES</span></span>

### <span data-ttu-id="080db-108">Exemplo 1: obter o token de SSO de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="080db-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="080db-109">Esse comando obtém o token de SSO de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="080db-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="080db-110">OS</span><span class="sxs-lookup"><span data-stu-id="080db-110">PARAMETERS</span></span>

### <span data-ttu-id="080db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080db-111">-DefaultProfile</span></span>
<span data-ttu-id="080db-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="080db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="080db-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="080db-113">-Name</span></span>
<span data-ttu-id="080db-114">Especifica o nome da instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="080db-114">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="080db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="080db-115">-ResourceGroupName</span></span>
<span data-ttu-id="080db-116">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="080db-116">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="080db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080db-117">CommonParameters</span></span>
<span data-ttu-id="080db-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="080db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080db-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="080db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080db-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="080db-120">INPUTS</span></span>

### <span data-ttu-id="080db-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="080db-121">None</span></span>
<span data-ttu-id="080db-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="080db-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="080db-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="080db-123">OUTPUTS</span></span>

### <span data-ttu-id="080db-124">System. String</span><span class="sxs-lookup"><span data-stu-id="080db-124">System.String</span></span>

## <span data-ttu-id="080db-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="080db-125">NOTES</span></span>

## <span data-ttu-id="080db-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="080db-126">RELATED LINKS</span></span>

[<span data-ttu-id="080db-127">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="080db-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)



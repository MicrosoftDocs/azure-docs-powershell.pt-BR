---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595666"
---
# <span data-ttu-id="e05fa-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="e05fa-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="e05fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e05fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e05fa-103">Obtém um link com um token de SSO para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e05fa-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="e05fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e05fa-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e05fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e05fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e05fa-106">O cmdlet **Get-AzApiManagementSsoToken** retorna um link (URL) que contém um token de logon único (SSO) para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e05fa-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="e05fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e05fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e05fa-108">Exemplo 1: obter o token de SSO de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="e05fa-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="e05fa-109">Esse comando obtém o token de SSO de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e05fa-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="e05fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="e05fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e05fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05fa-111">-DefaultProfile</span></span>
<span data-ttu-id="e05fa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e05fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e05fa-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e05fa-113">-Name</span></span>
<span data-ttu-id="e05fa-114">Especifica o nome da instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e05fa-114">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="e05fa-116">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e05fa-116">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05fa-117">CommonParameters</span></span>
<span data-ttu-id="e05fa-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05fa-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05fa-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e05fa-120">INPUTS</span></span>

### <span data-ttu-id="e05fa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e05fa-121">System.String</span></span>

## <span data-ttu-id="e05fa-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e05fa-122">OUTPUTS</span></span>

### <span data-ttu-id="e05fa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e05fa-123">System.String</span></span>

## <span data-ttu-id="e05fa-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e05fa-124">NOTES</span></span>

## <span data-ttu-id="e05fa-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e05fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="e05fa-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e05fa-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598095"
---
# <span data-ttu-id="09a84-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="09a84-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="09a84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09a84-102">SYNOPSIS</span></span>
<span data-ttu-id="09a84-103">Obtém um link com um token de SSO para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="09a84-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="09a84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09a84-104">SYNTAX</span></span>

### <span data-ttu-id="09a84-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="09a84-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09a84-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09a84-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09a84-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09a84-107">DESCRIPTION</span></span>
<span data-ttu-id="09a84-108">O cmdlet **Get-AzApiManagementSsoToken** retorna um link (URL) que contém um token de logon único (SSO) para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="09a84-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="09a84-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09a84-109">EXAMPLES</span></span>

### <span data-ttu-id="09a84-110">Exemplo 1: obter o token de SSO de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="09a84-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="09a84-111">Esse comando obtém o token de SSO de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="09a84-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="09a84-112">OS</span><span class="sxs-lookup"><span data-stu-id="09a84-112">PARAMETERS</span></span>

### <span data-ttu-id="09a84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a84-113">-DefaultProfile</span></span>
<span data-ttu-id="09a84-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09a84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09a84-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a84-115">-InputObject</span></span>
<span data-ttu-id="09a84-116">Instância do PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="09a84-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="09a84-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="09a84-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a84-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="09a84-118">-Name</span></span>
<span data-ttu-id="09a84-119">Especifica o nome da instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="09a84-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a84-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a84-120">-ResourceGroupName</span></span>
<span data-ttu-id="09a84-121">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="09a84-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09a84-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a84-122">CommonParameters</span></span>
<span data-ttu-id="09a84-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a84-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a84-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09a84-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a84-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09a84-125">INPUTS</span></span>

### <span data-ttu-id="09a84-126">System. String</span><span class="sxs-lookup"><span data-stu-id="09a84-126">System.String</span></span>

## <span data-ttu-id="09a84-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09a84-127">OUTPUTS</span></span>

### <span data-ttu-id="09a84-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09a84-128">System.String</span></span>

## <span data-ttu-id="09a84-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09a84-129">NOTES</span></span>

## <span data-ttu-id="09a84-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09a84-130">RELATED LINKS</span></span>

[<span data-ttu-id="09a84-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="09a84-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



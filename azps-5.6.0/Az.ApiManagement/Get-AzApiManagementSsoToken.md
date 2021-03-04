---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: eae199f28314db5aa50fa3247b46f02a407802fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892271"
---
# <span data-ttu-id="13321-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="13321-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="13321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13321-102">SYNOPSIS</span></span>
<span data-ttu-id="13321-103">Obtém um link com um token SSO para um portal de gerenciamento implantado de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="13321-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="13321-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="13321-104">SYNTAX</span></span>

### <span data-ttu-id="13321-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13321-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13321-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="13321-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13321-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13321-107">DESCRIPTION</span></span>
<span data-ttu-id="13321-108">O cmdlet **Get-AzApiManagementSsoToken** retorna um link (URL) contendo um único token de conexão (SSO) para um portal de gerenciamento implantado de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="13321-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="13321-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13321-109">EXAMPLES</span></span>

### <span data-ttu-id="13321-110">Exemplo 1: Obter o token SSO de um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="13321-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="13321-111">Este comando obtém o token SSO de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="13321-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="13321-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="13321-112">PARAMETERS</span></span>

### <span data-ttu-id="13321-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13321-113">-DefaultProfile</span></span>
<span data-ttu-id="13321-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="13321-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13321-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13321-115">-InputObject</span></span>
<span data-ttu-id="13321-116">Instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="13321-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="13321-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="13321-117">This parameter is required.</span></span>

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

### <span data-ttu-id="13321-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13321-118">-Name</span></span>
<span data-ttu-id="13321-119">Especifica o nome da instância de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="13321-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="13321-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13321-120">-ResourceGroupName</span></span>
<span data-ttu-id="13321-121">Especifica o nome do grupo de recursos no qual existe o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="13321-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="13321-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13321-122">CommonParameters</span></span>
<span data-ttu-id="13321-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13321-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13321-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13321-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13321-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13321-125">INPUTS</span></span>

### <span data-ttu-id="13321-126">System.String</span><span class="sxs-lookup"><span data-stu-id="13321-126">System.String</span></span>

## <span data-ttu-id="13321-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="13321-127">OUTPUTS</span></span>

### <span data-ttu-id="13321-128">System.String</span><span class="sxs-lookup"><span data-stu-id="13321-128">System.String</span></span>

## <span data-ttu-id="13321-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="13321-129">NOTES</span></span>

## <span data-ttu-id="13321-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13321-130">RELATED LINKS</span></span>

[<span data-ttu-id="13321-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="13321-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110844"
---
# <span data-ttu-id="4b09a-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="4b09a-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="4b09a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b09a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b09a-103">Obtém um link com um token SSO para um portal de gerenciamento implantado de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4b09a-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="4b09a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b09a-104">SYNTAX</span></span>

### <span data-ttu-id="4b09a-105">ExpandedParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b09a-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b09a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b09a-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b09a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b09a-107">DESCRIPTION</span></span>
<span data-ttu-id="4b09a-108">O cmdlet **Get-AzApiManagementSsoToken** retorna um link (URL) contendo um único token de SSO (sign-on) para um portal de gerenciamento implantado de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4b09a-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="4b09a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b09a-109">EXAMPLES</span></span>

### <span data-ttu-id="4b09a-110">Exemplo 1: Obter o token SSO de um serviço de Gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="4b09a-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="4b09a-111">Esse comando obtém o token SSO de um serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4b09a-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="4b09a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b09a-112">PARAMETERS</span></span>

### <span data-ttu-id="4b09a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b09a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b09a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4b09a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b09a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b09a-115">-InputObject</span></span>
<span data-ttu-id="4b09a-116">Instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4b09a-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="4b09a-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="4b09a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="4b09a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b09a-118">-Name</span></span>
<span data-ttu-id="4b09a-119">Especifica o nome da instância de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4b09a-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="4b09a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b09a-120">-ResourceGroupName</span></span>
<span data-ttu-id="4b09a-121">Especifica o nome do grupo de recursos no qual existe o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="4b09a-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="4b09a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b09a-122">CommonParameters</span></span>
<span data-ttu-id="4b09a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b09a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b09a-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b09a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b09a-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b09a-125">INPUTS</span></span>

### <span data-ttu-id="4b09a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4b09a-126">System.String</span></span>

## <span data-ttu-id="4b09a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b09a-127">OUTPUTS</span></span>

### <span data-ttu-id="4b09a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b09a-128">System.String</span></span>

## <span data-ttu-id="4b09a-129">Notas</span><span class="sxs-lookup"><span data-stu-id="4b09a-129">NOTES</span></span>

## <span data-ttu-id="4b09a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b09a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4b09a-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4b09a-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



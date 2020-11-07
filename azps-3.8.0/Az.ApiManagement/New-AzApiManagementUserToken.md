---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941921"
---
# <span data-ttu-id="8d018-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="8d018-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="8d018-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d018-102">SYNOPSIS</span></span>
<span data-ttu-id="8d018-103">Gera um token de acesso compartilhado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="8d018-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="8d018-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d018-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d018-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d018-105">DESCRIPTION</span></span>
<span data-ttu-id="8d018-106">O cmdlet **New-AzApiManagementUserToken** gera um token de acesso compartilhado para um usuário especificado</span><span class="sxs-lookup"><span data-stu-id="8d018-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="8d018-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d018-107">EXAMPLES</span></span>

### <span data-ttu-id="8d018-108">Exemplo 1: gerar um token de acesso compartilhado para usuário git</span><span class="sxs-lookup"><span data-stu-id="8d018-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="8d018-109">Esse script Obtém o usuário git configurado no serviço ApiManagement e gera um token de acesso compartilhado usando a chave primária válida por 8 horas.</span><span class="sxs-lookup"><span data-stu-id="8d018-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="8d018-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d018-110">PARAMETERS</span></span>

### <span data-ttu-id="8d018-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8d018-111">-Context</span></span>
<span data-ttu-id="8d018-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8d018-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8d018-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d018-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d018-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d018-114">-DefaultProfile</span></span>
<span data-ttu-id="8d018-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d018-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d018-116">-Vencimento</span><span class="sxs-lookup"><span data-stu-id="8d018-116">-Expiry</span></span>
<span data-ttu-id="8d018-117">Vencimento do token.</span><span class="sxs-lookup"><span data-stu-id="8d018-117">Expiry of the Token.</span></span>
<span data-ttu-id="8d018-118">Se não for especificado, o token será criado para expirar após 8 horas.</span><span class="sxs-lookup"><span data-stu-id="8d018-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="8d018-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8d018-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d018-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8d018-120">-KeyType</span></span>
<span data-ttu-id="8d018-121">Chave de usuário a ser usada ao gerar o token.</span><span class="sxs-lookup"><span data-stu-id="8d018-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="8d018-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8d018-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d018-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="8d018-123">-UserId</span></span>
<span data-ttu-id="8d018-124">Identificador do usuário existente.</span><span class="sxs-lookup"><span data-stu-id="8d018-124">Identifier of existing user.</span></span>
<span data-ttu-id="8d018-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d018-125">This parameter is required.</span></span>

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

### <span data-ttu-id="8d018-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d018-126">CommonParameters</span></span>
<span data-ttu-id="8d018-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d018-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d018-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d018-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d018-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d018-129">INPUTS</span></span>

### <span data-ttu-id="8d018-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d018-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d018-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8d018-131">System.String</span></span>

### <span data-ttu-id="8d018-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="8d018-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="8d018-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8d018-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8d018-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d018-134">OUTPUTS</span></span>

### <span data-ttu-id="8d018-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="8d018-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="8d018-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d018-136">NOTES</span></span>

## <span data-ttu-id="8d018-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d018-137">RELATED LINKS</span></span>

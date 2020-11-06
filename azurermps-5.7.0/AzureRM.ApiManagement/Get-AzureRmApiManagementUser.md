---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429915"
---
# <span data-ttu-id="d12d7-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="d12d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d12d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d12d7-103">Obtém um ou mais usuários.</span><span class="sxs-lookup"><span data-stu-id="d12d7-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d12d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d12d7-104">SYNTAX</span></span>

### <span data-ttu-id="d12d7-105">GeAllUsers (padrão)</span><span class="sxs-lookup"><span data-stu-id="d12d7-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d12d7-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d12d7-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12d7-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d12d7-108">DESCRIPTION</span></span>
<span data-ttu-id="d12d7-109">O cmdlet **Get-AzureRmApiManagementUser** Obtém um usuário especificado ou todos os usuários, se nenhum usuário for especificado.</span><span class="sxs-lookup"><span data-stu-id="d12d7-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="d12d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d12d7-110">EXAMPLES</span></span>

### <span data-ttu-id="d12d7-111">Exemplo 1: obter todos os usuários</span><span class="sxs-lookup"><span data-stu-id="d12d7-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="d12d7-112">Esse comando obtém todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="d12d7-112">This command gets all users.</span></span>

### <span data-ttu-id="d12d7-113">Exemplo 2: obter um usuário por ID</span><span class="sxs-lookup"><span data-stu-id="d12d7-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="d12d7-114">Este comando obtém um usuário por ID.</span><span class="sxs-lookup"><span data-stu-id="d12d7-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="d12d7-115">Exemplo: obter usuários pelo sobrenome</span><span class="sxs-lookup"><span data-stu-id="d12d7-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="d12d7-116">Esse comando obtém os usuários que têm um sobrenome especificado, o mais completo.</span><span class="sxs-lookup"><span data-stu-id="d12d7-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="d12d7-117">Exemplo 4: obter um usuário por endereço de email</span><span class="sxs-lookup"><span data-stu-id="d12d7-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="d12d7-118">Esse comando obtém o usuário que tem o endereço de email especificado.</span><span class="sxs-lookup"><span data-stu-id="d12d7-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="d12d7-119">Exemplo 5: obter todos os usuários de um grupo</span><span class="sxs-lookup"><span data-stu-id="d12d7-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="d12d7-120">Esse comando obtém todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="d12d7-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="d12d7-121">OS</span><span class="sxs-lookup"><span data-stu-id="d12d7-121">PARAMETERS</span></span>

### <span data-ttu-id="d12d7-122">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d12d7-122">-Context</span></span>
<span data-ttu-id="d12d7-123">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d12d7-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12d7-124">-DefaultProfile</span></span>
<span data-ttu-id="d12d7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d12d7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12d7-126">-Email</span><span class="sxs-lookup"><span data-stu-id="d12d7-126">-Email</span></span>
<span data-ttu-id="d12d7-127">Especifica o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="d12d7-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="d12d7-128">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por email.</span><span class="sxs-lookup"><span data-stu-id="d12d7-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="d12d7-129">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="d12d7-130">-FirstName</span></span>
<span data-ttu-id="d12d7-131">Especifica o primeiro nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="d12d7-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="d12d7-132">Se esse parâmetro for especificado, esse cmdlet localizará um usuário por nome.</span><span class="sxs-lookup"><span data-stu-id="d12d7-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="d12d7-133">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d12d7-134">-GroupId</span></span>
<span data-ttu-id="d12d7-135">Especifica o identificador do grupo.</span><span class="sxs-lookup"><span data-stu-id="d12d7-135">Specifies the group identifier.</span></span>
<span data-ttu-id="d12d7-136">Se especificado, esse cmdlet localiza todos os usuários dentro do grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="d12d7-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="d12d7-137">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="d12d7-138">-LastName</span></span>
<span data-ttu-id="d12d7-139">Especifica o último nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d12d7-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="d12d7-140">Se especificado, esse cmdlet localiza os usuários por sobrenome.</span><span class="sxs-lookup"><span data-stu-id="d12d7-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="d12d7-141">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-142">-Estado</span><span class="sxs-lookup"><span data-stu-id="d12d7-142">-State</span></span>
<span data-ttu-id="d12d7-143">Especifica o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="d12d7-143">Specifies the user state.</span></span>
<span data-ttu-id="d12d7-144">Se especificado, esse cmdlet localiza os usuários nesse estado.</span><span class="sxs-lookup"><span data-stu-id="d12d7-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="d12d7-145">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="d12d7-146">-UserId</span></span>
<span data-ttu-id="d12d7-147">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="d12d7-147">Specifies a user ID.</span></span>
<span data-ttu-id="d12d7-148">Se especificado, esse cmdlet localiza o usuário por esse identificador.</span><span class="sxs-lookup"><span data-stu-id="d12d7-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="d12d7-149">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d12d7-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12d7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12d7-150">CommonParameters</span></span>
<span data-ttu-id="d12d7-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12d7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12d7-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12d7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12d7-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d12d7-153">INPUTS</span></span>

### <span data-ttu-id="d12d7-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d12d7-154">None</span></span>
<span data-ttu-id="d12d7-155">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d12d7-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d12d7-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d12d7-156">OUTPUTS</span></span>

### <span data-ttu-id="d12d7-157">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="d12d7-158">Os detalhes do usuário no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d12d7-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="d12d7-159">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="d12d7-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="d12d7-160">A lista de usuários no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="d12d7-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="d12d7-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d12d7-161">NOTES</span></span>

## <span data-ttu-id="d12d7-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d12d7-162">RELATED LINKS</span></span>

[<span data-ttu-id="d12d7-163">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="d12d7-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="d12d7-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d12d7-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)



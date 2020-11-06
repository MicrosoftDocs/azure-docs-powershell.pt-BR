---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: e82559ec366809613ba66af4c27a3b944869f074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433155"
---
# <span data-ttu-id="8eccb-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="8eccb-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="8eccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eccb-102">SYNOPSIS</span></span>
<span data-ttu-id="8eccb-103">Modifica uma senha de catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8eccb-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eccb-104">SYNTAX</span></span>

### <span data-ttu-id="8eccb-105">Especificar o nome e a porta do host (padrão)</span><span class="sxs-lookup"><span data-stu-id="8eccb-105">Specify host name and port (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eccb-106">Especificar o URI completo</span><span class="sxs-lookup"><span data-stu-id="8eccb-106">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eccb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eccb-107">DESCRIPTION</span></span>
<span data-ttu-id="8eccb-108">O cmdlet Set-AzureRmDataLakeAnalyticsCatalogCredential modifica uma senha de credencial associada a um catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8eccb-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="8eccb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eccb-109">EXAMPLES</span></span>

### <span data-ttu-id="8eccb-110">Exemplo 1: modificar a senha de uma credencial associada a uma conta</span><span class="sxs-lookup"><span data-stu-id="8eccb-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="8eccb-111">Este comando define a senha da credencial como a senha especificada em NewPassword.</span><span class="sxs-lookup"><span data-stu-id="8eccb-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="8eccb-112">OS</span><span class="sxs-lookup"><span data-stu-id="8eccb-112">PARAMETERS</span></span>

### <span data-ttu-id="8eccb-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="8eccb-113">-Account</span></span>
<span data-ttu-id="8eccb-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8eccb-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="8eccb-115">-Credential</span></span>
<span data-ttu-id="8eccb-116">Especifica o nome e a senha atual da credencial a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="8eccb-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8eccb-117">-CredentialName</span></span>
<span data-ttu-id="8eccb-118">Especifica o nome da credencial a ser modificada</span><span class="sxs-lookup"><span data-stu-id="8eccb-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="8eccb-119">-DatabaseHost</span></span>
<span data-ttu-id="8eccb-120">Especifica o nome do host da fonte de dados externa à qual a credencial pode se conectar no formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="8eccb-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8eccb-121">-DatabaseName</span></span>
<span data-ttu-id="8eccb-122">Especifica o nome do banco de dados na conta data Lake Analytics que mantém a credencial.</span><span class="sxs-lookup"><span data-stu-id="8eccb-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-123">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="8eccb-123">-NewPassword</span></span>
<span data-ttu-id="8eccb-124">Especifica a nova senha da credencial</span><span class="sxs-lookup"><span data-stu-id="8eccb-124">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-125">-Porta</span><span class="sxs-lookup"><span data-stu-id="8eccb-125">-Port</span></span>
<span data-ttu-id="8eccb-126">Especifica o número da porta usada para se conectar ao DatabaseHost especificado usando essa credencial.</span><span class="sxs-lookup"><span data-stu-id="8eccb-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-127">-URI</span><span class="sxs-lookup"><span data-stu-id="8eccb-127">-Uri</span></span>
<span data-ttu-id="8eccb-128">Especifica o URI (Uniform Resource Identifier) completo da fonte de dados externa à qual essa credencial pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="8eccb-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8eccb-129">-Confirm</span></span>
<span data-ttu-id="8eccb-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eccb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eccb-131">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eccb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eccb-132">-DefaultProfile</span></span>
<span data-ttu-id="8eccb-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eccb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eccb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eccb-134">CommonParameters</span></span>
<span data-ttu-id="8eccb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eccb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eccb-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eccb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eccb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eccb-137">INPUTS</span></span>

## <span data-ttu-id="8eccb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eccb-138">OUTPUTS</span></span>

### <span data-ttu-id="8eccb-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8eccb-139">None</span></span>

## <span data-ttu-id="8eccb-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eccb-140">NOTES</span></span>

## <span data-ttu-id="8eccb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eccb-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e004ac5d14b10ac2304a937cb029361524fc829e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596925"
---
# <span data-ttu-id="9e34c-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9e34c-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="9e34c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e34c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e34c-103">Obtém uma entrada na ACL de um catálogo ou item de catálogo na análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="9e34c-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9e34c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e34c-104">SYNTAX</span></span>

### <span data-ttu-id="9e34c-105">GetCatalogAclEntry (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e34c-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e34c-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="9e34c-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e34c-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="9e34c-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e34c-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9e34c-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e34c-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="9e34c-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e34c-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="9e34c-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e34c-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e34c-111">DESCRIPTION</span></span>
<span data-ttu-id="9e34c-112">O cmdlet **Get-AzDataLakeAnalyticsCatalogItemAclEntry** Obtém uma lista de entradas (ACEs) na lista de controle de acesso (ACL) de um catálogo ou item de catálogo na análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="9e34c-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9e34c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e34c-113">EXAMPLES</span></span>

### <span data-ttu-id="9e34c-114">Exemplo 1: obter a ACL para um catálogo</span><span class="sxs-lookup"><span data-stu-id="9e34c-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="9e34c-115">Esse comando obtém a ACL para o catálogo da conta do data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="9e34c-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9e34c-116">Exemplo 2: obter a entrada ACL do proprietário do usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="9e34c-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9e34c-117">Este comando obtém a entrada ACL do proprietário do usuário para o catálogo da conta do data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="9e34c-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9e34c-118">Exemplo 3: obter a entrada ACL do proprietário do grupo para um catálogo</span><span class="sxs-lookup"><span data-stu-id="9e34c-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9e34c-119">Este comando obtém a entrada ACL do proprietário do grupo para o catálogo da conta do data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="9e34c-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9e34c-120">Exemplo 4: obter a ACL para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="9e34c-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="9e34c-121">Este comando obtém a ACL para o banco de dados da conta do data Lake Analytics especificada</span><span class="sxs-lookup"><span data-stu-id="9e34c-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9e34c-122">Exemplo 5: obter a entrada ACL do proprietário de um usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="9e34c-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9e34c-123">Este comando obtém a entrada ACL do proprietário do usuário para o banco de dados da conta especificada do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="9e34c-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="9e34c-124">Exemplo 6: obter a entrada ACL do proprietário de um grupo para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="9e34c-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="9e34c-125">Esse comando obtém a entrada ACL do proprietário do grupo para o banco de dados da conta especificada do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="9e34c-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="9e34c-126">OS</span><span class="sxs-lookup"><span data-stu-id="9e34c-126">PARAMETERS</span></span>

### <span data-ttu-id="9e34c-127">-Conta</span><span class="sxs-lookup"><span data-stu-id="9e34c-127">-Account</span></span>
<span data-ttu-id="9e34c-128">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9e34c-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9e34c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e34c-129">-DefaultProfile</span></span>
<span data-ttu-id="9e34c-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e34c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e34c-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="9e34c-131">-GroupOwner</span></span>
<span data-ttu-id="9e34c-132">Obter entrada de ACL do catálogo para proprietário do grupo</span><span class="sxs-lookup"><span data-stu-id="9e34c-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e34c-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="9e34c-133">-ItemType</span></span>
<span data-ttu-id="9e34c-134">Especifica o tipo de catálogo ou item (ns) de catálogo.</span><span class="sxs-lookup"><span data-stu-id="9e34c-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="9e34c-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e34c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e34c-136">Catálogo</span><span class="sxs-lookup"><span data-stu-id="9e34c-136">Catalog</span></span>
- <span data-ttu-id="9e34c-137">Base</span><span class="sxs-lookup"><span data-stu-id="9e34c-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e34c-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9e34c-138">-Path</span></span>
<span data-ttu-id="9e34c-139">Especifica o caminho do data Lake Analytics de um catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="9e34c-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="9e34c-140">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="9e34c-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e34c-141">-Userowner</span><span class="sxs-lookup"><span data-stu-id="9e34c-141">-UserOwner</span></span>
<span data-ttu-id="9e34c-142">Obtenha a entrada ACL do catálogo para proprietário do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e34c-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e34c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e34c-143">CommonParameters</span></span>
<span data-ttu-id="9e34c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e34c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e34c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e34c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e34c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e34c-146">INPUTS</span></span>

### <span data-ttu-id="9e34c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9e34c-147">System.String</span></span>

### <span data-ttu-id="9e34c-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="9e34c-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="9e34c-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e34c-149">OUTPUTS</span></span>

### <span data-ttu-id="9e34c-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="9e34c-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="9e34c-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e34c-151">NOTES</span></span>

## <span data-ttu-id="9e34c-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e34c-152">RELATED LINKS</span></span>

[<span data-ttu-id="9e34c-153">O U-SQL agora oferece controle de acesso no nível do banco de dados</span><span class="sxs-lookup"><span data-stu-id="9e34c-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="9e34c-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9e34c-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="9e34c-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9e34c-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

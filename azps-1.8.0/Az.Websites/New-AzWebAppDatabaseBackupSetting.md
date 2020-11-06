---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598327"
---
# <span data-ttu-id="7942a-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="7942a-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="7942a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7942a-102">SYNOPSIS</span></span>

## <span data-ttu-id="7942a-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7942a-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7942a-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7942a-104">DESCRIPTION</span></span>
<span data-ttu-id="7942a-105">O cmdlet **New-AzWebAppDatabaseBackupSetting** cria uma nova configuração de backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7942a-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="7942a-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7942a-106">EXAMPLES</span></span>

### <span data-ttu-id="7942a-107">1:</span><span class="sxs-lookup"><span data-stu-id="7942a-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="7942a-108">Cria uma configuração de backup de banco de dados (cadeia de conexão) do tipo sqlazure para o aplicativo especificado ContosoWebApp que está dentro do grupo de recursos-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="7942a-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7942a-109">OS</span><span class="sxs-lookup"><span data-stu-id="7942a-109">PARAMETERS</span></span>

### <span data-ttu-id="7942a-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7942a-110">-ConnectionString</span></span>
<span data-ttu-id="7942a-111">Cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="7942a-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7942a-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="7942a-112">-ConnectionStringName</span></span>
<span data-ttu-id="7942a-113">Nome da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="7942a-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7942a-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="7942a-114">-DatabaseType</span></span>
<span data-ttu-id="7942a-115">Tipo de banco de dados (por exemplo, "sqlazure" ou "MySql")</span><span class="sxs-lookup"><span data-stu-id="7942a-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="7942a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7942a-116">-DefaultProfile</span></span>
<span data-ttu-id="7942a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7942a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7942a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7942a-118">-Name</span></span>
<span data-ttu-id="7942a-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="7942a-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7942a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7942a-120">CommonParameters</span></span>
<span data-ttu-id="7942a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7942a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7942a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7942a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7942a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7942a-123">INPUTS</span></span>

### <span data-ttu-id="7942a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7942a-124">System.String</span></span>

## <span data-ttu-id="7942a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7942a-125">OUTPUTS</span></span>

### <span data-ttu-id="7942a-126">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="7942a-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="7942a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7942a-127">NOTES</span></span>

## <span data-ttu-id="7942a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7942a-128">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431585"
---
# <span data-ttu-id="54901-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="54901-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="54901-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54901-102">SYNOPSIS</span></span>
<span data-ttu-id="54901-103">Obtém a política de detecção de ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54901-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54901-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54901-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54901-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54901-105">DESCRIPTION</span></span>
<span data-ttu-id="54901-106">O cmdlet **Get-AzureRmSqlDatabaseThreatDetectionPolicy** Obtém a política de detecção de ameaças de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54901-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="54901-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém a política.</span><span class="sxs-lookup"><span data-stu-id="54901-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="54901-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54901-108">EXAMPLES</span></span>

### <span data-ttu-id="54901-109">Exemplo 1: obter a política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="54901-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="54901-110">Este comando obtém a política de detecção de ameaças para um banco de dados chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="54901-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="54901-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="54901-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="54901-112">OS</span><span class="sxs-lookup"><span data-stu-id="54901-112">PARAMETERS</span></span>

### <span data-ttu-id="54901-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54901-113">-DatabaseName</span></span>
<span data-ttu-id="54901-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54901-114">Specifies the name of a database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54901-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54901-115">-DefaultProfile</span></span>
<span data-ttu-id="54901-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54901-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54901-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54901-117">-ResourceGroupName</span></span>
<span data-ttu-id="54901-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="54901-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54901-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="54901-119">-ServerName</span></span>
<span data-ttu-id="54901-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="54901-120">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54901-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54901-121">-Confirm</span></span>
<span data-ttu-id="54901-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54901-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54901-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54901-123">-WhatIf</span></span>
<span data-ttu-id="54901-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54901-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54901-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54901-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54901-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54901-126">CommonParameters</span></span>
<span data-ttu-id="54901-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54901-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54901-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54901-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54901-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54901-129">INPUTS</span></span>

###  
<span data-ttu-id="54901-130">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54901-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="54901-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54901-131">OUTPUTS</span></span>

### <span data-ttu-id="54901-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="54901-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="54901-133">Esse cmdlet retorna um objeto **Model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="54901-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="54901-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54901-134">NOTES</span></span>

## <span data-ttu-id="54901-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54901-135">RELATED LINKS</span></span>

[<span data-ttu-id="54901-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="54901-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)




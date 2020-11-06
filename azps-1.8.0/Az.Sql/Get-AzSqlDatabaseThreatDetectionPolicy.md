---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599011"
---
# <span data-ttu-id="4a907-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a907-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="4a907-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a907-102">SYNOPSIS</span></span>
<span data-ttu-id="4a907-103">Obtém a política de detecção de ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a907-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="4a907-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a907-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a907-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a907-105">DESCRIPTION</span></span>
<span data-ttu-id="4a907-106">O cmdlet **Get-AzSqlDatabaseThreatDetectionPolicy** Obtém a política de detecção de ameaças de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4a907-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="4a907-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém a política.</span><span class="sxs-lookup"><span data-stu-id="4a907-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="4a907-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a907-108">EXAMPLES</span></span>

### <span data-ttu-id="4a907-109">Exemplo 1: obter a política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4a907-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="4a907-110">Este comando obtém a política de detecção de ameaças para um banco de dados chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="4a907-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="4a907-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a907-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="4a907-112">OS</span><span class="sxs-lookup"><span data-stu-id="4a907-112">PARAMETERS</span></span>

### <span data-ttu-id="4a907-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a907-113">-DatabaseName</span></span>
<span data-ttu-id="4a907-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a907-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="4a907-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a907-115">-DefaultProfile</span></span>
<span data-ttu-id="4a907-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4a907-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a907-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a907-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a907-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4a907-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4a907-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4a907-119">-ServerName</span></span>
<span data-ttu-id="4a907-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="4a907-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="4a907-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a907-121">-Confirm</span></span>
<span data-ttu-id="4a907-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a907-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a907-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a907-123">-WhatIf</span></span>
<span data-ttu-id="4a907-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a907-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a907-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a907-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a907-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a907-126">CommonParameters</span></span>
<span data-ttu-id="4a907-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a907-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a907-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a907-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a907-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a907-129">INPUTS</span></span>

### <span data-ttu-id="4a907-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a907-130">System.String</span></span>

## <span data-ttu-id="4a907-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a907-131">OUTPUTS</span></span>

### <span data-ttu-id="4a907-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4a907-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="4a907-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a907-133">NOTES</span></span>

## <span data-ttu-id="4a907-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a907-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a907-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a907-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)




---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262640"
---
# <span data-ttu-id="88166-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="88166-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="88166-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88166-102">SYNOPSIS</span></span>
<span data-ttu-id="88166-103">Obtém detalhes de uma configuração do Active Directory para arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="88166-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="88166-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88166-104">SYNTAX</span></span>

### <span data-ttu-id="88166-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="88166-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88166-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88166-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88166-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88166-107">DESCRIPTION</span></span>
<span data-ttu-id="88166-108">O cmdlet **Get-AzNetAppFilesActiveDirectory** Obtém detalhes de uma configuração de contas do anf do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88166-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="88166-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88166-109">EXAMPLES</span></span>

### <span data-ttu-id="88166-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88166-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="88166-111">Esse comando obtém a configuração de anúncio chamada MyADConfigName para a conta do Azure NetApp Files (ANF) chamada MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="88166-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="88166-112">OS</span><span class="sxs-lookup"><span data-stu-id="88166-112">PARAMETERS</span></span>

### <span data-ttu-id="88166-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88166-113">-AccountName</span></span>
<span data-ttu-id="88166-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="88166-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88166-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="88166-115">-AccountObject</span></span>
<span data-ttu-id="88166-116">A conta para o novo objeto do Active Directory</span><span class="sxs-lookup"><span data-stu-id="88166-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88166-117">-ActiveDirectoryid</span><span class="sxs-lookup"><span data-stu-id="88166-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="88166-118">O ActiveDirectoryid do Active Directory do ANF</span><span class="sxs-lookup"><span data-stu-id="88166-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88166-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88166-119">-DefaultProfile</span></span>
<span data-ttu-id="88166-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88166-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88166-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88166-121">-ResourceGroupName</span></span>
<span data-ttu-id="88166-122">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="88166-122">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88166-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88166-123">CommonParameters</span></span>
<span data-ttu-id="88166-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88166-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88166-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88166-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88166-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88166-126">INPUTS</span></span>

### <span data-ttu-id="88166-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="88166-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="88166-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88166-128">OUTPUTS</span></span>

### <span data-ttu-id="88166-129">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="88166-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="88166-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88166-130">NOTES</span></span>

## <span data-ttu-id="88166-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88166-131">RELATED LINKS</span></span>

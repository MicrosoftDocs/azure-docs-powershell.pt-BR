---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: 5e2b13cd4c2586b15cc526aad3d922441b40265c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598292"
---
# <span data-ttu-id="1ce0d-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="1ce0d-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="1ce0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ce0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce0d-103">Definir nomes de configuração do slot para aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="1ce0d-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="1ce0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ce0d-104">SYNTAX</span></span>

### <span data-ttu-id="1ce0d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1ce0d-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ce0d-106">S2</span><span class="sxs-lookup"><span data-stu-id="1ce0d-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ce0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ce0d-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce0d-108">O cmdlet **set-AzWebAppSlotConfigName** marca as configurações do aplicativo e as cadeias de conexão como configurações do slot</span><span class="sxs-lookup"><span data-stu-id="1ce0d-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="1ce0d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ce0d-109">EXAMPLES</span></span>

### <span data-ttu-id="1ce0d-110">1:</span><span class="sxs-lookup"><span data-stu-id="1ce0d-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="1ce0d-111">Esse comando Remove todas as configurações do aplicativo e cadeias de conexão do aplicativo Web ContosoWebApp associados ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="1ce0d-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1ce0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ce0d-112">PARAMETERS</span></span>

### <span data-ttu-id="1ce0d-113">-AppSettingnames</span><span class="sxs-lookup"><span data-stu-id="1ce0d-113">-AppSettingNames</span></span>
<span data-ttu-id="1ce0d-114">Matriz de cadeias de nomes de configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1ce0d-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-115">-ConnectionStringnames</span><span class="sxs-lookup"><span data-stu-id="1ce0d-115">-ConnectionStringNames</span></span>
<span data-ttu-id="1ce0d-116">Matriz de cadeias de nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="1ce0d-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce0d-117">-DefaultProfile</span></span>
<span data-ttu-id="1ce0d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ce0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce0d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ce0d-119">-Name</span></span>
<span data-ttu-id="1ce0d-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1ce0d-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="1ce0d-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="1ce0d-122">Opção remover todos os nomes de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1ce0d-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="1ce0d-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="1ce0d-124">Opção remover todos os nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="1ce0d-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ce0d-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1ce0d-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1ce0d-127">-WebApp</span></span>
<span data-ttu-id="1ce0d-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="1ce0d-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce0d-129">CommonParameters</span></span>
<span data-ttu-id="1ce0d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce0d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce0d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ce0d-132">INPUTS</span></span>

### <span data-ttu-id="1ce0d-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="1ce0d-133">System.String[]</span></span>

### <span data-ttu-id="1ce0d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ce0d-134">System.String</span></span>

### <span data-ttu-id="1ce0d-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1ce0d-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1ce0d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ce0d-136">OUTPUTS</span></span>

### <span data-ttu-id="1ce0d-137">Microsoft. Azure. Management. WebSites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="1ce0d-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="1ce0d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ce0d-138">NOTES</span></span>

## <span data-ttu-id="1ce0d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ce0d-139">RELATED LINKS</span></span>
